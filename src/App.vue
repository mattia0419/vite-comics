<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooterUp from './components/AppFooterUp.vue';
import AppFooterDown from './components/AppFooterDown.vue';
export default {
  components: {
    AppHeader,
    AppMain,
    AppFooterUp,
    AppFooterDown
  }
}
</script>




<template>
  <header>
    <AppHeader></AppHeader>

  </header>
  <main>
    <div class="container">
      <div class="content">
        <h2> --- Content goes here --- </h2>
      </div>
    </div>

    <AppMain></AppMain>


  </main>
  <footer>
    <AppFooterUp></AppFooterUp>
    <AppFooterDown></AppFooterDown>
  </footer>
</template>




<style lang="scss">
@use './assets/general.scss';
@use './assets/partial/_mixins.scss' as *;
@use './assets/partial/_variables.scss' as *;
@import url('https://fonts.googleapis.com/css2?family=Fira+Sans&family=Raleway&display=swap');

body {
  background-color: black;
  font-family: 'Raleway', sans-serif;
}

.content {
  width: 100%;
  height: 13vh;
  @include center('vertically');

  h2 {
    color: $color_secondary;
  }
}

.container {
  @include center('orizzontaly');
  width: 1000px;
  height: 100%;
  margin: auto;

}

footer {
  width: 100vw;
  height: 40vh;
  background-image: url(./assets/img/footer-bg.jpg);
}
</style>