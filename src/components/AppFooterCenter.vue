<script>
    export default {
        data() {
            return {
                list: [
                    {
                        title: "dc comics",
                        links: [
                            "Characters",
                            "Movies",
                            "TV",
                            "Games",
                            "Videos",
                            "News"
                        ]
                    },
                    {
                        title: "shop",
                        links: [
                            "Shop DC",
                            "Shop DC Collectibles"
                        ]
                    },
                    {
                        title: "DC",
                        links: [
                            "Terms Of Use",
                            "Privacy policy (New)",
                            "Ad Choices",
                            "Advertising",
                            "Jobs",
                            "Subscriptions",
                            "Talent Workshops",
                            "CPSC Certificates",
                            "Ratings",
                            "Shop Help",
                            "Contact Us"
                        ]
                    },
                    {
                        title: "sites",
                        links: [
                            "DC",
                            "MAD Magazine",
                            "DC Kids",
                            "DC Universe",
                            "DC Power Visa"
                        ]
                    }
                ]
            }
        }
    }

</script>

<template>

    <section>
        <div class="container">

            
           <div id="footer-center-links">

               <div v-for="element in list" id="footer-center-link">
                    
                   <h2>{{ element.title }}</h2>
                   <ul>
                       <li v-for="link in element.links">
                           <a href="">{{ link }}</a>
                       </li>
                   </ul>
               </div>

           </div> 

            <div id="footer-center-logo">
                <img src="/img/dc-logo-bg.png" alt="">
            </div>

        </div>
    </section>

</template>

<style scoped lang="scss">

    @use 'style/_variables.scss' as *;
    @use 'style/_mixins.scss' as *;

    section {
        background-image: url("/img/footer-bg.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        .container {
            @include centerMaxWidth();

            display: flex;
            justify-content: space-between;

            height: 350px;

            #footer-center-links {

                display: flex;
                flex-flow: column wrap;
                gap: 1rem;

                padding: 2rem 0;

                #footer-center-link {

                    h2 {
                        font-size: medium;
                        text-transform: uppercase;
                        color: white;
                    }
        
                    ul li a {
                        text-decoration: none;
                        font-size: smaller;
                        color: $lighter-gray;
                    }
                    
                }

            }

            #footer-center-logo {
                display: flex;
                align-items: center;

                height: 100%;
                overflow-y: hidden;
            }

        }

    }

</style>