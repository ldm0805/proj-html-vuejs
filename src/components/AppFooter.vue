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
                        'Bookmark',
                        'Features',
                        'SiteMap',
                        'Lists',
                        'Conctact Us'
                    ]
                }
            ]
        }
    },
}
</script>
<template lang="">
        <AppFooterInfo :menuNav="menuNav"/> 
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
</style>