<script>
export default {
    props: {
        menuFooter: Array
    }
}
</script>
<template lang="">
    <div class="details-cont">

        <div class="d-flex px-2">
            <!-- Address info -->
            <div class="address">
                <ul class="gray">
                    <li>
                        <h5>Address Info</h5>
                    </li>
                    <li>
                        <div class="d-flex text-white align-items-start">
                            <div>
                                <i class="fa-solid fa-location-dot"></i>
                            </div>
                            <span>60 29th Street San Francisco, CA 94110 507-Union Trade Center, United States of America</span> 
                        </div>
                    </li>
                    <li>
                        <i class="fa-solid fa-phone"></i>
                        <span>(+00) 123-456-789</span>
                    </li>
                    <li class="hover-y">
                        <i class="fa-solid fa-envelope"></i>
                        <span>demo@example.com</span>
                    </li>
                </ul>
            </div>
            <!-- Information -->
            <div class="col-middle">
                <ul class="d-flex">
                    <li class="mx-5" v-for="(item, index) in menuFooter" :key="index">
                        <a :href="item.url"><h5>{{ item.label }}</h5></a>
                        <ul>
                            <li v-for="(item, index) in item.details" :key="index"><a href="#"><span>{{ item }}</span></a></li>
                        </ul>
                    </li>
                </ul>
            </div>
            <!-- newsletter -->
            <div>
                <div>
                    <h5>Our Newsletter</h5>
                    <span>There are many variations of spanassages of form humour or randomised</span>
                </div>
                <div class="tnp tnp-widget toggle-block">
                    <form>
                        <div class="tnp-field tnp-field-email">
                            <input class="tnp-email p-2" type="email" name="ne" id="tnp-1" value="" required="">
                                <input class="tnp-submit" type="submit" value="Subscribe">
                            
                        </div>
                        </form>
                        <div class="social">
                            <ul class="d-flex">
                                <li><i class="fa-brands fa-facebook-f"></i></li>
                                <li><i class="fa-brands fa-twitter"></i></li>
                                <li><i class="fa-brands fa-google-plus-g"></i></li>
                                <li><i class="fa-brands fa-skype"></i></li>
                                <li><i class="fa-brands fa-instagram"></i></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
                <div class="copyright d-flex justify-content-between px-2">
                    <div>
                        <span>Copyright ?? 2023 Codezeel</span>
                    </div>
                    <div class="social">
                            <ul class="d-flex">
                                <li><i class="fa-brands fa-cc-mastercard"></i></li>
                                <li><i class="fa-brands fa-cc-visa"></i></li>
                                <li><i class="fa-brands fa-cc-amex"></i></li>
                                <li><i class="fa-brands fa-cc-paypal"></i></li>
                                <li><i class="fa-brands fa-google-pay"></i></li>
                            </ul>
                        </div>
            </div>
        </div>
        </template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.details-cont {
    display: flex;
    flex-direction: column;
    background-image: url('./../../public/img/footer-bg.png');
    padding: 80px 0em;

    h5 {
        font-weight: bold;
        color: white;
    }

    ul {
        list-style-type: none;
        padding: 0;

        li {
            .fa-solid {
                color: $yellow;
                margin-right: .5em;
            }

            i {
                color: white;
                font-size: 20px;
            }

            span {
                &:hover {
                    color: $yellow;
                }
            }

            .fa-facebook-f {
                &:hover {
                    cursor: pointer;
                    color: $yellow;
                }
            }

            .fa-twitter {
                &:hover {
                    cursor: pointer;
                    color: rgb(65, 65, 255);
                }
            }

            .fa-skype {
                &:hover {
                    cursor: pointer;
                    color: rgb(65, 65, 255);
                }
            }

            .fa-instagram {
                &:hover {
                    cursor: pointer;
                    color: rgb(209, 52, 131);
                }
            }

            .fa-google-plus-g {
                &:hover {
                    cursor: pointer;
                    color: red;
                }
            }

            .hover-y {
                span {
                    cursor: pointer;

                    &:hover {
                        color: $yellow;
                    }
                }
            }
        }

    }

    .copyright {
        border-top: 1px solid #515772;
    }


    .col-middle {
        padding: 0em 10em;
    }
}

span {
    color: $gray;
}

a {
    text-decoration: none;

}

.fa-brands {
    font-size: 20px;
}

.tnp-field {
    position: relative;
}

.tnp .tnp-submit {
    position: absolute;
    height: 45px;
    width: 45px;
    font-size: 0;
    right: 150px;
    color: #000000;
    background-image: url(../../public/img/newsletter.png);
    background-attachment: scroll;
    background-repeat: no-repeat;
    background-position: center 13px;
    background-color: transparent;
    padding: 0px;
    -webkit-transition: none;
    -moz-transition: none;
    -o-transition: none;
    transition: none;
    border: 0;

    &:hover {
        background-position: center -51px;
        border-color: $yellow;
    }
}

.social {
    margin-top: 1.2em;

    .fa-brands {
        padding-right: 1em
    }

}
</style>