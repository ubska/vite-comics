<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            navList: [
                {
                    title: "CHARACTERS",
                    url: "/characters",
                    active: false,
                },
                {
                    title: "COMICS",
                    url: "/comics",
                    active: true,
                },
                {
                    title: "MOVIES",
                    url: "/movies",
                    active: false,
                },
                {
                    title: "TV",
                    url: "/tv",
                    active: false,
                },
                {
                    title: "GAMES",
                    url: "/games",
                    active: false,
                },
                {
                    title: "COLLECTIBLES",
                    url: "/collectibles",
                    active: false,
                },
                {
                    title: "VIDEOS",
                    url: "/videos",
                    active: false,
                },
                {
                    title: "FANS",
                    url: "/fans",
                    active: false,
                },
                {
                    title: "NEWS",
                    url: "/news",
                    active: false,
                },
                {
                    title: "SHOP",
                    url: "/shop",
                    active: false,
                },
            ],
        };
    },
};
</script>

<template>
    <header>
        <div class="container">
            <!-- logo -->
                <div class="logo">
                    <a href="#">
                        <img src="../assets/dc-logo.png" alt="" />
                    </a>
                </div>
            <!-- menu di navigazione -->
                <div class="navbar">
                    <ul>
                        <li v-for="(link, index) in navList" :key="index">
                            <a :class="{ active: link.active }" :href="link.url">{{
                            link.title
                            }}</a>
                        </li>
                    </ul>
                </div>
        </div>
        <div id="jumbotron">
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;


header{
    text-align: center;

    ul{
        list-style: none;
        margin: 2.5rem 1rem 4rem;
        @include center('both');
        gap: 2%;
    }
    a {
        text-decoration: none;
    }
  
    .container{
        @include center('both');
        justify-content: space-between;
    }

  #jumbotron {
    background-image: url(../assets/jumbotron.jpg);
    background-size: cover;
    height: 25rem;
    width: 100%;
}
}
</style>