<script>
import AppJumbotron from './AppJumbotron.vue';
import AppSingleSerie from './AppSingleSerie.vue';

export default{
    data(){
      return{

        comicSeries: [
            {
                thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                price: "$19.99",
                series: "Action Comics",
                type: "comic book"
            },
            {
                thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                price: "$3.99",
                series: "American Vampire 1976",
                type: "comic book"
            },
            {
                thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                price: "$16.99",
                series: "Aquaman",
                type: "graphic novel"
            },
            {
                thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                price: "$2.99",
                series: "Batgirl",
                type: "comic book"
            },
            {
                thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                price: "$3.99",
                series: "Batman",
                type: "comic book"
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                price: "$2.99",
                series: "Batman Beyond",
                type: "comic book"
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                price: "$3.99",
                series: "Batman/Superman",
                type: "comic book"
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                price: "$4.99",
                series: "Batman/Superman Annual",
                type: "comic book"
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                price: "$5.99",
                series: "Batman: The Joker War Zone",
                type: "comic book"
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                price: "$6.99",
                series: "Batman: Three Jokers",
                type: "comic book"
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                price: "$4.99",
                series: "Batman: White Knight Presents: Harley Quinn",
                type: "comic book"
            },
            {
                thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
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
            align-items: flex-start;
            flex-wrap: wrap;
            gap: 20px;

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