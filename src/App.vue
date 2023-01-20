<script>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"
export default {

  components: {
    AppHeader: AppHeader,
    AppMain: AppMain,
    AppFooter: AppFooter,
  }
}
</script>




<template>

  <AppHeader />

  <AppMain />

  <AppFooter />

</template>




<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

img {
  width: 100%;
  height: auto;
}

header,
main,
footer,
div,
nav {
  border: 1px solid black;
}
</style>
