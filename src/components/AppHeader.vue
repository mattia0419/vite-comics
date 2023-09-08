<script>
export default {
    data() {
        return {
            links: [
                'CHARACTERS',
                'COMICS',
                'MOVIES',
                'TV',
                'GAMES',
                'COLLECTIBLES',
                'VIDEOS',
                'FANS',
                'NEWS',
                'SHOP'
            ]
        };
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>
            <div v-for="link in links" class="link-list">
                <a href="#">{{ link }}</a>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/general.scss';
@use '../assets/partial/_variables.scss' as *;
@use '../assets/partial/_mixins.scss' as *;

header {
    background-color: $color_secondary;
    height: 13vh;
    margin-top: 20px;
}

.container {
    @include center();
    width: 1000px;
    height: 100%;
    margin: auto;

}

.logo {
    height: 100%;
    width: 50%;
    @include center('vertically');
    justify-content: flex-start;

    img {
        width: 80px;
    }


}

.link-list {
    margin-left: 20px;
    font-size: 12px;
    height: 100%;
    cursor: pointer;
    @include center('vertically');
    justify-content: flex-end;

    a {
        text-decoration: none;
        color: black;
    }
}

.link-list:hover {
    border-bottom: solid 5px $color_primary;

    a {
        color: $color_primary;
    }
}
</style>