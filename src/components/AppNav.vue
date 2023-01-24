<script>
export default {
    props: {
        menuNav: Array
    }
}
</script>
<template lang="">
        <nav class="nav_cont">
            <ul>
                <!-- For per la navbar + click sugli elementi per assegnare la classe active -->
                <li v-for="(item, index) in menuNav" :key="index">
                    <a :href="item.url">
                        {{ item.label }}
                        <ul class="d-flex flex-column">
                            <li class="my-2" v-for="(item, index) in item.details" :key="index"><a href="#"><span>{{ item }}</span></a></li>
                        </ul>
                    </a>
                </li>
            </ul>
        </nav>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.nav_cont {

    @include justify_content_between;
    margin-top: 1em;
    text-align: center;

    ul {
        margin: 2rem 1rem;
        @include center;
        list-style-type: none;
        color: $white;

        .active {
            color: $primary;
            border-bottom: 3px solid $primary;
            padding-bottom: 2em;
        }

        li a {
            padding: 1em;
            font-size: 16px;
            text-decoration: none;
            transition: border 0.3s;
            @include upbold;

        }
    }
}
</style>