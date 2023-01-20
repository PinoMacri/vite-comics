<script>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"
import "@fontsource/open-sans"
import "@fontsource/open-sans-condensed"
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

;

body {
  font-family: "Open Sans", sans-serif;
}

;

header,
main,
footer,
div {
  border: 1px solid black;
}
</style>
