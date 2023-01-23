<script>
import { store } from './store.js';
import AppHeader from './components/AppHeader.vue';
export default {
  components: {
    AppHeader,
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
  </div>
</template>

<style  lang="scss">
@use './styles/generals.scss' as *;
</style>
