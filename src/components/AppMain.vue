<script>
import AppJumbotron from './AppJumbotron.vue';
import AppSingleSerie from './AppSingleSerie.vue';

export default{
    data(){
      return{

        comicSeries: [
            {
                thumb: "https://picsum.photos/150/200",
                price: "$19.99",
                series: "Action Comics",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$3.99",
                series: "American Vampire 1976",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$16.99",
                series: "Aquaman",
                type: "graphic novel"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$2.99",
                series: "Batgirl",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$3.99",
                series: "Batman",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$2.99",
                series: "Batman Beyond",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$3.99",
                series: "Batman/Superman",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$4.99",
                series: "Batman/Superman Annual",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$5.99",
                series: "Batman: The Joker War Zone",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$6.99",
                series: "Batman: Three Jokers",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$4.99",
                series: "Batman: White Knight Presents: Harley Quinn",
                type: "comic book"
            },
            {
                thumb: "https://picsum.photos/150/200",
                price: "$16.99",
                series: "Catwoman",
                type: "graphic novel"
            }
        ]
      
      }
    },

    components:{
        AppJumbotron,
        AppSingleSerie
    }
    
  }
</script>

<template>

    <AppJumbotron></AppJumbotron>

    <main>

        <div id="current-series-label">
            current series
        </div>
        
        <div id="current-series-container">
            <AppSingleSerie v-for="item in comicSeries" :img="item.thumb" :title="item.series"></AppSingleSerie>
        </div>

        <button>Load more</button>

    </main>

</template>

<style scoped lang="scss">

    @use 'style/_variables.scss' as *;
    @use 'style/_mixins.scss' as *;

    main {
        position: relative;

        padding: 3rem 0 2rem;

        text-align: center;
        color: white;
        background-color: $dark-grey;

        #current-series-label {
            position: absolute;
            top: 0;
            left: 0;
            transform: translate(30%, -50%);
            
            padding: .3em 1em;

            text-transform: uppercase;
            color: white;
            background-color: $skyblue;
            }

        #current-series-container {
            @include centerMaxWidth();
            @include centerFlex();
            flex-wrap: wrap;
            gap: 10px;

            height: 100%;
            margin-bottom: 2rem;
        }

        button {
            padding: .5em 3em;
            
            text-align: center;
            text-transform: uppercase;
            border: none;
            color: white;
            background-color: $skyblue;
            cursor: pointer;
        }

    }

</style>