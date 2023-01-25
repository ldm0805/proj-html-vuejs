<script>
export default {
    props: {
        menuNav: Array
    },
}
</script>
<template lang="">
        <nav class="nav_cont">
            <ul>
                <li class="dropdown_" v-for="(item, index) in menuNav" :key="index">
                       <span class="title">
                        {{ item.label }}
                    </span>
                    <li>
                            <div class="h-100" v-for="(item, index) in item.details" :key="index">
                                <a class="dropdown-content_" href="#">{{ item }}</a>
                            </div>
                    </li>
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

        li {
            height: 60px;

        }

        li a {
            color: $gray;
            padding: 1em;
            font-size: 16px;
            text-decoration: none;
            transition: border 0.3s;


            &:hover {
                color: $yellow;
            }
        }
    }
}

.title {
    @include upbold;

    &:hover {
        color: $yellow;
        cursor: pointer;
    }
}


.dropdown_ {
    position: relative;
}

.dropdown-content_ {
    display: none;
    position: absolute;
    background-color: $darkblue;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
    z-index: 1;
}

.dropdown-content_ {
    a {
        &:hover {
            background-color: #ddd;
        }
    }
}

.dropdown_:hover .dropdown-content_ {
    display: block;
}
</style>