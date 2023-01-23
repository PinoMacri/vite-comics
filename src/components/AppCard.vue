<script>
export default {
    name: "AppCard",
    props: {
        cards: Array
    }
}
</script>

<template>

    <div class="singleCard" v-for="card in cards" :key="card.series">
        <img class="img-fluid" :src="card.thumb" :alt="card.series">
        <p>{{ card.series }}</p>
    </div>

</template>

<style lang="scss" scoped>
@use "../assets/sass/mixin" as*;

.singleCard {
    width: calc(100% / 6);
    height: 200px;
    overflow: hidden;
    padding: 30px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: 0px -10px;
    }
}
</style>