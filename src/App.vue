<script>
  import AppHeader from "./components/AppHeader.vue";
  import AppMain from "./components/AppMain.vue";
  import AppFooterTop from "./components/AppFooterTop.vue";
  import AppFooterCenter from "./components/AppFooterCenter.vue";

  export default {
        components: {
            AppHeader,
            AppMain,
            AppFooterTop,
            AppFooterCenter
        }
    } 

</script>

<template>

  <AppHeader></AppHeader>

  <AppMain></AppMain>

  <footer>
    
    <AppFooterTop></AppFooterTop>
    <AppFooterCenter></AppFooterCenter>

  </footer>

</template>

<style scoped>

</style>
