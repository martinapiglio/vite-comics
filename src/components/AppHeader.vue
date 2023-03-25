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

    @use 'style/_variables.scss' as *;
    @use 'style/_mixins.scss' as *;

    header .container {
        @include centerFlex();
        @include centerMaxWidth();
        
        height: 5rem;
        
        * {
            @include centerFlex();
            height: 100%;
        }

        #header-left {
            padding: .8rem 0;

            img {
                cursor: pointer;
            }
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

                transition: 0.1s;
            }

            li:hover {
                border-bottom: 4px solid $skyblue;
                cursor: pointer;
            }

        } 

    }

</style>