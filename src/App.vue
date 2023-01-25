<script>
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
import AppSpecialCategory from './components/AppSpecialCategory.vue';
// import AppService from './components/AppService.vue'
// import AppJumboSlider from './components/AppJumboSlider.vue';
import AppJoystick from './components/AppJoystick.vue';
export default {
  components: {
    AppHeader,
    AppFooter,
    AppSpecialCategory,
    // AppService,
    // AppJumboSlider,
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
  <div>
    <AppHeader />
    <AppSpecialCategory />
    <AppJoystick />
    <AppFooter />
    <!-- <AppService /> -->
    <!-- <AppJumboSlider /> -->
  </div>
</template>

<style  lang="scss">
@use './styles/generals.scss' as *;
</style>
