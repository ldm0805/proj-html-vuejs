<script>
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppSpecialCategory from './components/AppSpecialCategory.vue';
import AppProfile from './components/AppProfile.vue'
import AppSponsor from './components/AppSponsor.vue';
import AppGameBlogs from './components/AppGameBlogs.vue'
import AppService from './components/AppService.vue'
import AppJoystick from './components/AppJoystick.vue';
export default {
  components: {
    AppHeader,
    AppFooter,
    AppSpecialCategory,
    AppService,
    AppProfile,
    AppSponsor,
    AppGameBlogs,
    AppJoystick,
  },
  data() {
    return {
      store,
    }
  },
}
</script>

<template>
  <div class="d-flex flex-column gap-3">
    <AppHeader />
    <AppSpecialCategory />
    <AppJoystick />
    <AppProfile />
    <AppService />
    <AppGameBlogs />
    <AppSponsor />
    <AppFooter />
  </div>
</template>

<style  lang="scss">
@use './styles/generals.scss' as *;
</style>
