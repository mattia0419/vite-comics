<script>
export default {
    props: {
        img: String,
        text: String
    }
}
</script>


<template>
    <div class="card">
        <img :src="img" alt="">
        <p>{{ text }}</p>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/general.scss';
@use '../assets/partial/_variables.scss' as *;
@use '../assets/partial/_mixins.scss' as *;
</style>