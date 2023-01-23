<script>
export default {
    name: "AppJumbotron",
}
</script>

<template>
    <div class="jumbotron">
        <div class="container">
            <button>CURRENT SERIES</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../assets/sass/variables" as*;

div.jumbotron {
    padding: 20px;
    height: 400px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;

    button {
        position: absolute;
        bottom: 0;
        transform: translatey(50%);
        background-color: $text-color-blue ;
        border: none;
        color: white;
        padding: 10px 30px;
        font-weight: 800;

        &:hover {
            color: gold;
            cursor: pointer;
        }
    }
}
</style>