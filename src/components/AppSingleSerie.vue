<script>
export default{
    data(){
      return{
      }
    },

    props:{
        img: String,
        title: String,
    }
    
  }

</script>

<template>

    <div class="card">

        <img :src="img" alt="">
        <div id="title">
            {{title}}
        </div>

    </div>

</template>

<style scoped lang="scss">

    @use 'style/_variables.scss' as *;
    @use 'style/_mixins.scss' as *;

    .card {
        width: calc(100% / 6 - (10px / 6 * 5));
        height: calc(100% / 2);

        #title {
            font-size: .8em;
            text-align: left;
            text-transform: uppercase;
        }

        img {
            width: 100%;
        }
    }


</style>