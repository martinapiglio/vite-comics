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
        width: calc(100% / 6 - (20px / 6 * 5));
        height: calc(100% / 2);

        img {
            width: 100%;
            aspect-ratio: 1;
            object-fit: cover;

            cursor: pointer;
        }

        #title {
            font-size: .8em;
            text-align: left;
            text-transform: uppercase;

            transition: 1s;
        }

        #title:hover {
            text-decoration: underline;
            cursor: pointer;
        }
    }


</style>