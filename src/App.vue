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
@import url('https://fonts.googleapis.com/css2?family=Fira+Sans&display=swap');


body {
  background-color: black;
  font-family: 'Fira Sans', sans-serif;
}
</style>