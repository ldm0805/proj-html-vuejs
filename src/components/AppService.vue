<script>
export default {

}
</script>
<template>
    <div class="cont-delivery">
        <div class="service-content">
            <span class="icon-image">

            </span>
            <h5>Free Delivery</h5>
            <span>Free shipping on all order</span>
        </div>
        <div class="service-content">
            <span class="icon-image-1">

            </span>
            <h5>Free Delivery</h5>
            <span>Free shipping on all order</span>
        </div>
        <div class="service-content">
            <span class="icon-image-2">

            </span>
            <h5>Free Delivery</h5>
            <span>Free shipping on all order</span>
        </div>
        <div class="service-content">
            <span class="icon-image-3">

            </span>
            <h5>Free Delivery</h5>
            <span>Free shipping on all order</span>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.cont-delivery {
    display: flex;
    justify-content: center;
}

.service-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0em 2em;
    color: white;

    .icon-image,
    .icon-image-1,
    .icon-image-2,
    .icon-image-3 {
        height: 55px;
        position: relative;
        width: 55px;
        float: left;
        -webkit-transition: all 0.5s ease;
        -moz-transition: all 0.5s ease;
        -o-transition: all 0.5s ease;
        transition: all 0.5s ease;
    }

    .icon-image {
        background: rgba(0, 0, 0, 0) url(../../public/img/service-icon.png) no-repeat scroll center -102px;


        &:hover {
            background-position: center 20px;
            border-color: $yellow;
        }
    }

    .icon-image-1 {
        background: rgba(0, 0, 0, 0) url(../../public/img/service-icon.png) no-repeat scroll center -327px;


        &:hover {
            background-position: center -215px;
            border-color: $yellow;
        }
    }

    .icon-image-2 {
        background: rgba(0, 0, 0, 0) url(../../public/img/service-icon.png) no-repeat scroll center -555px;

        &:hover {
            background-position: center -443px;
            border-color: $yellow;
        }
    }

    .icon-image-3 {
        background: rgba(0, 0, 0, 0) url(../../public/img/service-icon.png) no-repeat scroll center -778px;


        &:hover {
            background-position: center -670px;
            border-color: $yellow;
        }
    }

    h5 {
        @include upbold;

        &:hover {
            color: $yellow;
            cursor: pointer;
        }
    }
}


.service-list {
    .style-1 {
        position: relative;
    }
}

.service-list {
    display: inline-block;
    float: none;
    vertical-align: middle;
    width: 100%;
}

user agent stylesheet div {
    display: block;
}

.cz-service {
    text-align: center;
}

body {
    font-family: 'Poppins', Arial, Helvetica, sans-serif;
}
</style>