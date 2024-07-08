<script>
export default {
    name: 'FooterTop',
    data() {
        return {
            comics: [
                "Characters",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Videos",
                "News"
            ],
            shop: [
                "Shop DC",
                "Shop DC Collectibles"
            ],
            dc: [
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
            ],
            sites: [
                "DC",
                "MAD Magazine",
                "DC Kids",
                "DC Universe",
                "DC Power Visa"
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <!-- colonna di sinistra -->
            <div class="column">
                <h3>DC Comics</h3>
                <ul>
                    <li v-for="comic in comics"><a href="#">{{ comic }}</a></li>
                </ul>

                <h3>Shop</h3>
                <ul>
                    <li v-for="shop in shop"><a href="#">{{ shop }}</a></li>
                </ul>
            </div>
            <!-- colonna centrale -->
            <div class="column">
                <h3>DC</h3>
                <ul>
                    <li v-for="dc in dc"><a href="#">{{ dc }}</a></li>
                </ul>
            </div>
            <!-- colonna di destra -->
            <div class="column">
                <h3>Sites</h3>
                <ul>
                    <li v-for="site in sites"><a href="#">{{ site }}</a></li>
                </ul>
            </div>
            <div class="column">
                <img src="../assets/dc-logo-bg.png" alt="logo-dc">
            </div>
        </div>
        
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

footer{
    background: url(../assets/footer-bg.jpg);
    background-size: auto, cover;

    .container {
        display: flex;
        padding: 1.875rem 0;

        .column {
            margin-right: 1.25rem;

            h3 {
                color: white;
                text-transform: uppercase;
            }

            ul {
                margin: .625rem 0;

                li {
                    font-size: .875rem;
                    margin: .3125rem 0;

                    a {
                        color: rgb(172, 167, 167);
                        text-decoration: none;
                    }
                }

            }

        }
    }
}
</style>