<script>
    export default {
        data() {
            return {
                icons: [
                '/img/footer-facebook.png',
                '/img/footer-twitter.png',
                '/img/footer-youtube.png',
                '/img/footer-pinterest.png',
                '/img/footer-periscope.png',
                ]
            }
        }
    }

</script>

<template>

    <section>
        <div class="container">

            <div id="footer-bottom-left">
                <button>SIGN-UP NOW!</button>
            </div>

            <div id="footer-bottom-right">
                <span class="text">FOLLOW US</span>
                <div class="icons">
                    <img v-for="icon in icons" :src="icon" alt="">
                </div>
            </div>

        </div>
    </section>

</template>

<style scoped lang="scss">

    @use 'style/_variables.scss' as *;
    @use 'style/_mixins.scss' as *;

    section {
        background-color: $mid-dark-grey;

        .container {
            @include centerMaxWidth();
            @include centerFlex();

            padding: 1.5rem;

            #footer-bottom-left {

                button {
                    padding: .7rem;
                    border: 2px solid $skyblue;

                    color: white;
                    background-color: transparent;
                    cursor: pointer;

                    transition: 0.2s;
                }

                button:hover {
                    background-color: $skyblue;
                }

            }

            #footer-bottom-right {
                @include centerFlex();
                gap: .7rem;

                .text {
                    font-weight: bold;
                    color: $skyblue;
                }

                .icons {
                    @include centerFlex();
                    gap: .3rem;

                    img {
                        transform: scale(0.75);
                        cursor: pointer;
                    }

                }
            }
        }
    }
    

</style>