<script>
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
// import AppJoystick from './components/AppJoystick.vue';
export default {
  components: {
    AppHeader,
    AppFooter,
    // AppJoystick,
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
    <AppFooter />
    <!-- <AppJoystick /> -->
  </div>
</template>

<style  lang="scss">
@use './styles/generals.scss' as *;
</style>
