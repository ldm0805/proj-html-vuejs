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
                <h5 class="widget-title"><a href="#">Need Help?</a></h5>
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