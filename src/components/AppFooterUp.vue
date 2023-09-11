<script>
export default {
    data() {
        return {
            dcComics: [
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Videos',
                'News'
            ],
            shops: [
                'Shop DC',
                'Shop DC Collectibles'
            ],
            informations: [
                'Terms Of Use',
                'Privacy policy(New)',
                'Ad Choises',
                'Advertising',
                'Jobs',
                'Subscriptions',
                'Talent Workshops',
                'CPSC Certificates',
                'Ratings',
                'Shop Help',
                'Contact Us'
            ],
            sites: [
                'DC',
                'MAD Magazine',
                'DC Kids',
                'DC Universe',
                'DC Power Visa'
            ]
        }
    }
}

</script>


<template>
    <div class="container">
        <div class="section">
            <h3>DC COMICS</h3>
            <div class="list">
                <a v-for="dcComic in dcComics" href="#">{{ dcComic }}</a>
            </div>
            <h3>SHOP</h3>
            <div class="list">
                <a v-for="shop in shops" href="#">{{ shop }}</a>
            </div>
        </div>
        <div class="section">
            <h3>DC</h3>
            <div class="list">
                <a v-for="info in informations" href="#">{{ info }}</a>
            </div>
        </div>
        <div class="section">
            <h3>SITES</h3>
            <div class="list">
                <a v-for="site in sites" href="#">{{ site }}</a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/general.scss';
@use '../assets/partial/_variables.scss' as *;
@use '../assets/partial/_mixins.scss' as *;

.container {
    @include center();
    width: 1000px;
    height: 100%;
    margin: auto;
    justify-content: flex-start;
    align-items: flex-start;

}

h3 {
    color: $color_secondary;
    margin-bottom: 10px;
    margin-top: 10px;
}

.list {
    display: flex;
    flex-direction: column;

    a {
        text-decoration: none;
        color: lightgray;
        font-size: 13px;
        line-height: 20px;
    }
}

.section {

    margin-top: 25px;
    margin-right: 35px;
    margin-bottom: 25px;
}



a:hover {
    color: $color_secondary;
}
</style>