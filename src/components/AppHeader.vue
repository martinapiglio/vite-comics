<script>
    export default {
  data() {
    return {
      links: [
        'characters',
        'comics',
        'movies',
        'tv',
        'games',
        'collectibles',
        'videos',
        'fans',
        'news',
        'shop'
      ]
    };
  },
};
</script>

<template>

    <header>
        <div class="container">

            <div id="header-left">
                <img src="img/dc-logo.png" alt="">
            </div>

            <div id="header-right">

                <ul>
                    <li v-for="link in links">
                    {{ link }} </li>
                </ul>

            </div>

        </div>
    </header>

</template>

<style scoped lang="scss">

    $main-color: #0282f9;

    @mixin centerFlex() {
        display: flex;
        flex-flow: row nowrap;
        justify-content: space-between;
        align-items: center;
    }

    @mixin centerMaxWidth() {
        max-width: 980px;
        margin: auto;
    }
    header .container {
        @include centerFlex();
        @include centerMaxWidth();
        
        height: 5rem;
        
        * {
            @include centerFlex();
            height: 100%;
        }

        #header-right {

            ul {
                gap: 1rem;
                font-weight: bold;
                font-size: 12px;
                text-transform: uppercase;
            };

            li {
                
                border-bottom: 4px solid transparent;
            }

            li:hover {
                border-bottom: 4px solid $main-color;
                cursor: pointer;
            }

        } 


    }








</style>