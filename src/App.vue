<script>
  import AppHeader from "./components/AppHeader.vue";
  import AppContent from "./components/AppContent.vue";
  import AppNavbar from "./components/AppNavbar.vue";

  export default {
        components: {
            AppHeader,
            AppContent,
            AppNavbar
        }
    } 

</script>

<template>

  <AppHeader></AppHeader>

  <AppContent></AppContent>

  <AppNavbar></AppNavbar>

</template>

<style scoped>

</style>
