<script>
export default {
    data() {
        return {
            items: [
                {
                    image: 'buy-comics-digital-comics.png',
                    description: 'DIGITAL COMICS'
                },
                {
                    image: 'buy-comics-merchandise.png',
                    description: 'DC MERCHANDISE'
                },
                {
                    image: 'buy-comics-subscriptions.png',
                    description: 'SUBSCRIPTION'
                },
                {
                    image: 'buy-comics-shop-locator.png',
                    description: 'COMIC SHOP LOCATOR'
                },
                {
                    image: 'buy-dc-power-visa.svg',
                    description: 'DC POWER VISA'
                },

            ]
        }
    },
    methods: {
        buildingImagePath(imageName) {
            const imageURL = new URL('../assets/img/' + imageName, import.meta.url);
            console.log(imageURL);

            return imageURL.href;
        }
    }

}
</script>

<template>
    <div class="blu-content">
        <div class="container">
            <div class="card" v-for="item in items">
                <img :src="buildingImagePath(item.image)" alt="">
                <span>{{ item.description }}</span>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/general.scss';
@use '../assets/partial/_variables.scss' as *;
@use '../assets/partial/_mixins.scss' as *;

.container {
    @include center('orizzontaly');
    width: 1000px;
    height: 100%;
    margin: auto;
}

.blu-content {
    width: 100vw;
    height: 20vh;
    background-color: $color_primary;
}

.card {
    height: 100%;
    width: 200px;
    cursor: pointer;
    @include center();

    img {
        width: 35px;
    }

    span {
        color: $color_secondary;
        font-size: 13px;
        margin-left: 10px;
    }
}
</style>