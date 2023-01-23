<script>
export default {
    props: {
        menuFooter: Array
    }
}
</script>
<template lang="">
    <div>
        <ul>
            <li v-for="(item, index) in menuFooter" :key="index">
                <a :href="item.url">{{ item.label }}</a>
                <ul>
                    <li v-for="(item, index) in item.details" :key="index">{{ item }}</li>
                </ul>
            </li>
        </ul>
    </div>
</template>
<style lang="">
    
</style>