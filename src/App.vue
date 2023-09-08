<script>
import AppHeader from './components/AppHeader.vue';
export default {
  components: {
    AppHeader
  }
}
</script>




<template>
  <header>
    <AppHeader></AppHeader>
  </header>
</template>




<style lang="scss">
@use './assets/general.scss';

body {
  background-color: black;
}
</style>