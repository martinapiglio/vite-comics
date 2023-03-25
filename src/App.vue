<script>
  import AppHeader from "./components/AppHeader.vue";
  import AppMain from "./components/AppMain.vue";
  import AppFooterTop from "./components/AppFooterTop.vue";
  import AppFooterCenter from "./components/AppFooterCenter.vue";
  import AppFooterBottom from "./components/AppFooterBottom.vue"

  export default {
        components: {
            AppHeader,
            AppMain,
            AppFooterTop,
            AppFooterCenter,
            AppFooterBottom
        }
    } 

</script>

<template>

  <AppHeader></AppHeader>

  <AppMain></AppMain>

  <footer>
    
    <AppFooterTop></AppFooterTop>
    <AppFooterCenter></AppFooterCenter>
    <AppFooterBottom></AppFooterBottom>

  </footer>

</template>

<style scoped>

</style>
