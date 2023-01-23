<script>
import AppFooterInfo from './AppFooterInfo.vue';
export default {
    components: {
        AppFooterInfo
    },
    data() {
        return {
            menuFooter: [
                {
                    label: 'Information',
                    details: [
                        'Bookmark',
                        'Features',
                        'SiteMap',
                        'Lists',
                        'Conctact Us'
                    ]
                },
                {
                    label: 'Extras',
                    details: [
                        'Delivery',
                        'Cart',
                        'Terms conditions',
                        'My account',
                        'About us'
                    ]
                }
            ]
        }
    },
}
</script>
<template lang="">
        <AppFooterInfo :menuFooter="menuFooter"/> 
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
</style>