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
                <li class="dropdown_" v-for="(item, index) in menuNav" :key="index">
                    <a :href="item.url">
                        {{ item.label }}
                    </a>
                    <ul class="d-flex flex-column">
                        <li class="dropdown-content_" v-for="(item, index) in item.details" :key="index">
                            <a href="#">{{ item }}</a>
                        </li>
                    </ul>
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

.dropdown_ {
    position: relative;
    display: inline-block;
}

.dropdown-content_ {
    display: none;
    position: absolute;
    background-color: #f1f1f1;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
    z-index: 1;
}

.dropdown-content_ ul {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
}

.dropdown-content_ a:hover {
    background-color: #ddd;
}

.dropdown_:hover .dropdown-content_ {
    display: block;
}
</style>