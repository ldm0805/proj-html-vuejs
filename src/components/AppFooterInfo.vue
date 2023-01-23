<script>
export default {
    props: {
        menuFooter: Array
    }
}
</script>
<template lang="">
    <div class="details-cont">
        <!-- Address info -->
        <div class="address">
            <ul>
                <li>
                    <h5>Address Info</h5>
                </li>
                <li>
                    <i class="fa-solid fa-location-dot"></i>
                    <span>60 29th Street San Francisco, CA 94110 507-Union Trade Center, United States of America</span> 
                </li>
                <li>
                    <i class="fa-solid fa-phone"></i>
                    <span>(+00) 123-456-789</span>
                </li>
                <li>
                    <i class="fa-solid fa-envelope"></i>
                    <span>demo@example.com</span>
                </li>
            </ul>
        </div>
        <!-- Information -->
        <div class="col-4">
            <ul>
                <li v-for="(item, index) in menuFooter" :key="index">
                    <a :href="item.url">{{ item.label }}</a>
                    <ul>
                        <li v-for="(item, index) in item.details" :key="index"><a href="#">{{ item }}</a></li>
                    </ul>
                </li>
            </ul>
        </div>
        <!-- newsletter -->
        <div class="newsletter">
            <h5>Our Newsletter</h5>
        <span>There are many variations of passages of form humour or randomised</span>
        <div class="input-group">
            <input type="text" class="form-control" placeholder="Recipient's username" aria-label="Recipient's username" aria-describedby="basic-addon2">
            <div class="input-group-append">
                <span class="input-group-text" id="basic-addon2">@example.com</span>
            </div>
        </div>
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
    
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.details-cont {
    display: flex;
    justify-content: space-between;

    ul {
        list-style-type: none;
    }
}
</style>