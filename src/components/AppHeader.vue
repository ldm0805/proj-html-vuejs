<script>
import AppNav from './AppNav.vue';
export default {
    components: {
        AppNav
    },
    data() {
        return {
            menuNav: [
                {
                    label: 'Home',

                },
                {
                    label: 'Shop',
                    details: [
                        'Top Rated Product',
                        'Product Category'
                    ]
                },
                {
                    label: 'Blog',
                    details: [
                        'Left Sidebar',
                        'Right Sidebar',
                        'Full Width'
                    ]
                },
                {
                    label: 'Media',
                    details: [
                        '2 Columns',
                        '3 Columns',
                        '4 Columns',
                    ],
                    details: [
                        '2 Columns',
                        '3 Columns',
                        '4 Columns',
                    ]

                },
                {
                    label: 'ShortCode',
                    details: [
                        'Accordions & Toggles',
                        'Buttons',
                        'Divider',
                        'Progress Bar & Pie Chart',
                        'Lists'
                    ],
                    details: [
                        'Services',
                        'Tabs',
                        'Map & Contact',
                        'Message Boxes',
                        'Pricing Table',

                    ]
                },
                {
                    label: 'Features',
                    details: [
                        'FAQs Page',
                        'Typography',
                        'Sitemap',
                        'About Us',
                        'Contact Us',
                        'Product Category'
                    ]
                },
            ]
        }
    },
}
</script>
<template lang="">
    <div class="top-header">
        <div class="left-cont">
            <h5 class="whislist-counter"><a href="#">WhishList(0)</a></h5>
            <div class="header-contact">
                <h5 class="widget-title "><a href="#">Need Help?</a></h5>
            </div>
        </div>
        <div class="right-cont">
            <h5 ><a href="#">Call 24/7 . 800-8754-987</a></h5>
        </div>
    </div>
    <div class="container_head">
        <img src="public\img\mob-logo.png" alt="">
        <AppNav :menuNav="menuNav"/>
        <div class="shop">
            <ul>
                <li>  
                    <div class="searchInputWrapper">
                        <input class="searchInput" type="text" placeholder='Ricerca'>
                        <i class="searchInputIcon fa fa-search"></i>
                    </div>
                    </li>
                <li><a href="#"><i class="fa-regular fa-user"></i></a> </li>
                <li><a href="#"><i class="fa-solid fa-bag-shopping"></i></a><span>(0)</span> </li>

            </ul>
        </div>
    </div>  
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.top-header {
    display: flex;
    justify-content: space-between;
    background-color: $darkblue;
    align-items: center;
    border-bottom: 1px solid #a6a6a66e;

    a {
        text-decoration: none;
        color: #a6a6a6;
        padding: 1em;
    }


    .whislist-counter {
        display: inline-block;
        vertical-align: top;
        padding: 13px 0px 11px;
        margin: 0px;
        position: relative;
        z-index: 9;
    }

    .header-contact {
        display: inline-block;
        position: relative;
        z-index: 9;
        padding: 12px 0px;
        margin: 0px;
        margin-left: 34px;
        vertical-align: top;


        &:before {
            content: "";
            border-right: 1px solid #342c3d;
            position: absolute;
            left: -20px;
            right: auto;
            top: 15px;
            height: 15px;
        }

    }
}

a:hover {
    color: $yellow;
}

.container_head {
    background-color: $darkblue;
    display: flex;
    justify-content: space-around;
    text-align: center;
    align-items: center;

    .widget-title:after {
        font-family: 'FontAwesome';
        font-size: 14px;
        content: "\F107";
        font-weight: normal;
        font-style: normal;
        padding-left: 5px;
        color: #a6a6a6;
    }

    .shop {
        display: flex;
        align-items: center;

        ul {
            display: flex;
            list-style-type: none;
            gap: 1em;
            font-size: 18px;
            margin: 0;

            li span {
                color: $yellow;
                padding: 0 .5em;
            }

            li a {
                color: white;

                &:hover {
                    color: $yellow;
                }
            }
        }
    }
}

.heading {
    margin-bottom: 1.5rem;
    font-size: 1.2rem;
}

.searchInputWrapper {
    position: relative;
}

.searchInput {
    width: 15rem;
    height: 2rem;
    padding: 0 1rem;
    border-radius: 2rem;
    border: none;
    transition: transform 0.1s ease-in-out;
}

::placeholder {
    color: #a1a1a1;
}

/* hide the placeholder text on focus */
:focus::placeholder {
    text-indent: -999px
}

.searchInput:focus {
    outline: none;
    transform: scale(1.1);
    transition: all 0.1s ease-in-out;
}

.searchInputIcon {
    position: absolute;
    right: 0.8rem;
    top: 0.5rem;
    color: #a1a1a1;
    transition: all 0.1s ease-in-out;
}

.container:focus-within>.searchInputWrapper>.searchInputIcon {
    right: 0.2rem;
}
</style>