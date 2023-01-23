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
                },
                {
                    label: 'Blog',
                },
                {
                    label: 'Media',
                },
                {
                    label: 'ShortCode',
                },
                {
                    label: 'Features',
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
                <h5 class=" dropdown"><a href="#">Need Help?</a></h5>
                <ul class="dropdown-menu">
    <li><a href="#">action 1</a></li>
    <li><a href="#">action 2</a></li>
    <li><a href="#">action 3</a></li>
    <li><a href="#">action 4</a></li>
  </ul>
            </div>
        </div>
        <div class="right-cont">
            <h5 ><a href="#">Call 24/7 . 800-8754-987</a></h5>
        </div>
    </div>
    <div class="container_head">
        <img src="src\assets\img\mob-logo.png" alt="">
        <AppNav :menuNav="menuNav"/>
    </div>  
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.dropdown {
    background: #7b1fa2;
    color: #fff;
    cursor: pointer;
    height: 50px;
    line-height: 50px;
    position: relative;
    width: 200px;
    text-align: center;
    text-decoration: none;
    z-index: 1;
    transform: perspective(1000px);
    -webkit-box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.12), 0 1px 5px 0 rgba(0, 0, 0, 0.2);
    box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.14), 0 3px 1px -2px rgba(0, 0, 0, 0.12), 0 1px 5px 0 rgba(0, 0, 0, 0.2);
}

.dropdown-menu {
    background-color: #fff;
    list-style-type: none;
    margin: 0;
    padding: 0;
    position: absolute;
    left: 0;
    opacity: 0;
    text-align: center;
    top: 0;
    visibility: hidden;
    z-index: -99999;
}

.dropdown-menu li:first-child {
    cursor: default;
}

.dropdown-menu a {
    color: #000;
    display: inline-block;
    width: 100%;
    text-decoration: none;
    -webkit-transition: all 1s;
    transition: all 1s;
}

.dropdown-menu a:hover {
    background: #ba68c8;
    color: #fff;
}

.dropdown:hover .dropdown-menu {
    background: #7b1fa2;
    opacity: 1;
    visibility: visible;
    top: 100%;
    width: 100%;
    -webkit-transition: all .5s, background, 2s .5s linear;
    transition: all .5s, background 2s .5s linear;
}

.top-header {
    display: flex;
    justify-content: space-between;
    background-color: $darkblue;
    align-items: center;
    border-bottom: 1px solid #a6a6a66e;

    a {
        text-decoration: none;
        color: #a6a6a6;
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
    @include justify_content_between;
    text-align: center;
}

.widget-title:after {
    font-family: 'FontAwesome';
    font-size: 14px;
    content: "\F107";
    font-weight: normal;
    font-style: normal;
    padding-left: 5px;
    color: #a6a6a6;
}
</style>