<script>
export default {
  data() {
    return {
        links: [
            {
                icon: 'img/buy-comics-digital-comics.png',
                title: 'digital comics'
            },
            {
                icon: 'img/buy-comics-merchandise.png',
                title: 'dc merchandise'
            },
            {
                icon: 'img/buy-comics-subscriptions.png',
                title: 'subscription'
            },
            {
                icon: 'img/buy-comics-shop-locator.png',
                title: 'comic shop locator'
            },
            {
                icon: 'img/buy-dc-power-visa.svg',
                title: 'dc power visa'
            }
        ]
    };
  },
};
</script>

<template>
    <section>
        <div class="container">
            <ul>
                <li v-for="link in links">
                    <img :src="link.icon" alt=""> {{ link.title }}
                </li>
            </ul>
        </div>
    </section>
</template>

<style scoped lang="scss">

@use 'style/_variables.scss' as *;
@use 'style/_mixins.scss' as *;

section {

    height: 8rem;
    color: white;
    background-color: $skyblue;

    * {
        height: 100%;
    }

    .container {
        @include centerMaxWidth();

        ul {
            @include centerFlex();
        }
    
        li {
            @include centerFlex();
            justify-content: flex-start;
            gap: .5em;
    
            font-size: 13px;
            text-transform: uppercase;
    
            img {
                height: 35%;
            }

        }

        li:last-child img {
            width: 25%;
        }
    }

}

</style>