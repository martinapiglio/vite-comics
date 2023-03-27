<script>
    import AppJumbotron from './AppJumbotron.vue';

export default{
    data(){
      return{
      
      }
    },

    components:{
        AppJumbotron
    }
    
  }
</script>

<template>
    <main>
        <AppJumbotron></AppJumbotron>
        <div class="container">
            

        </div>
    </main>
</template>

<style scoped lang="scss">

    @use 'style/_variables.scss' as *;
    @use 'style/_mixins.scss' as *;

    main {
    
    
    color: white;
    background-color: $dark-grey;
        .container {
        @include centerMaxWidth();
        @include centerFlex();

        height:100%;

        }
    }

</style>