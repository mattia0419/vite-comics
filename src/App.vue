<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooterUp from './components/AppFooterUp.vue';
import AppFooterDown from './components/AppFooterDown.vue';
import AppThumbsVue from './components/AppThumbs.vue';
export default {
  data() {
    return {
      books: [
        {
          "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          "price": "$19.99",
          "series": "Action Comics",
          "type": "comic book"
        },
        {
          "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          "price": "$3.99",
          "series": "American Vampire 1976",
          "type": "comic book"
        },
        {
          "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          "price": "$16.99",
          "series": "Aquaman",
          "type": "graphic novel"
        },
        {
          "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          "price": "$2.99",
          "series": "Batgirl",
          "type": "comic book"
        },
        {
          "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          "price": "$3.99",
          "series": "Batman",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          "price": "$2.99",
          "series": "Batman Beyond",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          "price": "$3.99",
          "series": "Batman/Superman",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          "price": "$4.99",
          "series": "Batman/Superman Annual",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          "price": "$5.99",
          "series": "Batman: The Joker War Zone",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          "price": "$6.99",
          "series": "Batman: Three Jokers",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          "price": "$4.99",
          "series": "Batman: White Knight Presents: Harley Quinn",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          "price": "$16.99",
          "series": "Catwoman",
          "type": "graphic novel"
        }
      ]
    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooterUp,
    AppFooterDown,
    AppThumbsVue
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
        <div class="card-container">

          <AppThumbsVue v-for="book in books" :img="book.thumb" :text="book.series"></AppThumbsVue>

        </div>
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

  @include center('orizzontally');


}

.card-container {
  width: 100%;
  color: $color_secondary;
  display: flex;
  flex-wrap: wrap;

  div {
    width: calc(100% / 6);
    padding: 15px;
  }

  img {
    max-width: 100%;
    height: 200px;
  }

  p {
    font-size: 12px;
  }


}

.container {
  @include center('orizzontaly');
  width: 1000px;
  height: 100%;
  margin: auto;

}

footer {
  width: 100%;
  background-image: url(./assets/img/footer-bg.jpg);
}
</style>