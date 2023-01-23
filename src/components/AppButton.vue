<script>
import "@fontsource/open-sans"
export default {
    name: "AppButton",
    props: {
        type: String,
        textbutton: String,
    }
}
</script>

<template>
    <div class="buttons">
        <button class="basic-style" :class="type">
            {{ textbutton }}
        </button>
    </div>

</template>

<style lang="scss" scoped>
@use "../assets/sass/variables" as*;

div.buttons {
    display: flex;
    justify-content: center;
    width: 100%;

    .basic-style {
        background-color: $text-color-blue ;
        padding: 10px 30px;
        border: none;
        color: white;
        font-weight: 900;
        margin-top: 30px;

        &:hover {
            cursor: pointer;
        }
    }

    button.type-1 {
        position: absolute;
        bottom: 0;
        left: 0;

        &:hover {
            color: gold;
        }
    }

    button.type-2 {

        &:hover {
            transform: scale(1.2);
        }
    }
}
</style>