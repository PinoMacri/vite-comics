<script>
import "@fontsource/open-sans"
export default {
    name: "AppButton",
}
</script>

<template>
    <div class="buttons">
        <button>LOAD MORE</button>
    </div>

</template>

<style lang="scss" scoped>
@use "../assets/sass/variables" as*;

div.buttons {
    display: flex;
    justify-content: center;
    width: 100%;

    button {
        background-color: $text-color-blue ;
        padding: 10px 30px;
        border: none;
        color: white;
        font-weight: 900;
        margin-top: 30px;

        &:hover {
            transform: scale(1.2);
            cursor: pointer;

        }
    }
}
</style>