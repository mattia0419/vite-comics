<script>
export default {
    data() {
        return {
            imageSocial: [
                "footer-facebook.png",
                "footer-periscope.png",
                "footer-pinterest.png",
                "footer-twitter.png",
                "footer-youtube.png"
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
    <div class="footer-down">
        <div class="container">
            <div>
                <button class="sign-up-button">SIGN-UP NOW!</button>
            </div>
            <div class="follow">
                <h5>FOLLOW US</h5>
                <div v-for="image in imageSocial">
                    <img :src="buildingImagePath(image)" alt="">
                </div>
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use '../assets/general.scss';
@use '../assets/partial/_variables.scss' as *;
@use '../assets/partial/_mixins.scss' as *;

.footer-down {
    width: 100%;
    height: 9vh;
    background-color: #303030;
}

.container {
    @include center('vertically');
    width: 1000px;
    height: 100%;
    margin: auto;
    justify-content: space-between;
}

.sign-up-button {
    padding: 10px;
    background-color: transparent;
    color: white;
    border: solid 2px $color_primary;
}



.follow {
    @include center('vertically');

    h5 {
        color: $color_primary;
        margin-right: 25px;
    }

    img {
        margin-left: 15px;
        width: 30px;
        cursor: pointer;
    }
}
</style>