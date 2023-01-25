<script>
export default {

}
</script>
<template>
    <div class="special-title">
        <h3 class="text-white">Special Category</h3>
        <div class="border_"></div>
    </div>
    <div class="img-category">
        <div class="img-block">
            <img src="public\img\category-image-01-446x550_t.jpg" alt="superhero_image">
            <div class="cat_description">
                <a class="cat_name" href="https://capricathemes.com/wordpress/WCM04/WCM040086/product-category/batman/"
                    title="Batman">
                    <h5> Batman</h5>
                </a>
                <a class="read-more" href="https://capricathemes.com/wordpress/WCM04/WCM040086/product-category/batman/"
                    title="Batman">Shop Now</a>
            </div>
        </div>
        <div class="img-block">
            <img src="public\img\category-image-02-446x550_t.jpg" alt="superhero_image">
            <div class="cat_description">
                <a class="cat_name" href="https://capricathemes.com/wordpress/WCM04/WCM040086/product-category/batman/"
                    title="Batman">
                    <h5> Bayonetta</h5>
                </a>
                <a class="read-more" href="https://capricathemes.com/wordpress/WCM04/WCM040086/product-category/batman/"
                    title="Batman">Shop Now</a>
            </div>
        </div>
        <div class="img-block">
            <img src="public\img\category-image-03-446x550_t.jpg" alt="superhero_image">
            <div class="cat_description">
                <a class="cat_name" href="https://capricathemes.com/wordpress/WCM04/WCM040086/product-category/batman/"
                    title="Batman">
                    <h5> Dark Souls</h5>
                </a>
                <a class="read-more" href="https://capricathemes.com/wordpress/WCM04/WCM040086/product-category/batman/"
                    title="Batman">Shop Now</a>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.special-title {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    margin: 3em 0em;

    .border_ {
        margin: 1em;
        width: 2.5em;
        border-bottom: 1px solid $yellow;
    }
}

img {
    &:hover {
        filter: brightness(1.55);
        transition: all 1s ease-in;
        ;
    }
}

.img-category {
    display: flex;
    justify-content: space-around;


    .img-block {
        position: relative;


        .cat_description {
            box-sizing: border-box;
            padding: 25px 13px 15px;
            text-align: left;
            position: absolute;
            width: 100%;
            bottom: 0;
            background: rgb(29 20 39 / 75%);
            -webkit-transition: all 500ms ease;
            -moz-transition: all 500ms ease;
            -o-transition: all 500ms ease;
            transition: all 500ms ease;

            &:hover {
                background: rgb(29 20 39 / 90%);
            }

            a {
                text-decoration: none;
                color: $yellow;
                border-bottom: 1px solid $yellow;
                padding-bottom: 5px;

                &:hover {
                    border: none;
                }

                h5 {
                    color: white;
                }
            }
        }
    }
}
</style>