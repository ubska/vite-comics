<script>
export default {
    name: 'AppProducts',
     data() {
        return {
            buttons: [
                {
                    image: '../src/assets/buy-comics-digital-comics.png',
                    text: 'Digital Comics'
                },
                {
                    image: '../src/assets/buy-comics-merchandise.png',
                    text: 'DC Merchandise'
                },
                {
                    image: '../src/assets/buy-comics-subscriptions.png',
                    text: 'Subscription'
                },
                {
                    image: '../src/assets/buy-comics-shop-locator.png',
                    text: 'Comic Shop Locator'
                },
                {
                    image: '../src/assets/buy-dc-power-visa.svg',
                    text: 'DC Power VISA'
                }
            ]
        }
    },
}
</script>

<template>
    <main>
        <div class="container">
            <div v-for="button in buttons" class="button">
                <div class="image">
                    <img :src="button.image" :alt="button.text">
                </div>
                <div class="text"><a href="#">{{ button.text }}</a></div>
            </div>
        </div>
    </main>
      
</template>


<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

main{
    background-color: rgba(64, 64, 240, 0.975);

      .container{
        @include center('both');
        justify-content: space-between;
        flex-wrap: wrap;
    }

    .button{
        @include center('both');
        justify-content: space-between;
        align-items: center;
        width: 150px;
        margin: 10px;
        text-align: center;
    }

    a {
        text-decoration: none;
        color: white;
        margin-top: 10px;
    }

    // .image{
    //     width: 100%;
    //     height: 100px;
    //     overflow: hidden;
    // }
    img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
</style>