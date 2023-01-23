<script>
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  components: {
    AppHeader,
    AppFooter,
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
  </div>
</template>

<style  lang="scss">
@use './styles/generals.scss' as *;
</style>
