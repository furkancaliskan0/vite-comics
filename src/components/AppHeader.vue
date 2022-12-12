<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    tap: "true",
                },
                {
                    text: "COMICS",
                    url: "#",
                    tap: "false",
                },
                {
                    text: "MOVIES",
                    url: "#",
                    tap: "false",
                },
                {
                    text: "TV",
                    url: "#",
                    tap: "false",
                },
                {
                    text: "GAMES",
                    url: "#",
                    tap: "false",
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    tap: "false",
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    tap: "false",
                },
                {
                    text: "FANS",
                    url: "#",
                    tap: "false",
                },
                {
                    text: "NEWS",
                    url: "#",
                    tap: "false",
                },
                {
                    text: "SHOP",
                    url: "#",
                    tap: "false",
                }
            ]
        }
    }
}

</script>

<template>
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <a href="#">
                        <img src="../assets/images/dc-logo.png" alt="Dc-logo">
                    </a>
                </div>
                <li v-for="(link, index) in links" :key="index" class="active">
                    <a :href="link.url">{{ link.text }}</a>
                </li>
            </nav>
        </div>
    </header>
  </template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/mixins.scss' as *;
@use '../styles/partials/variables' as *;

header {
    margin: 0 auto;
    width: 100%;
    .container {
        width: 80%;
        margin: 0 auto;
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            .logo {
                width: 40%;
            }
            li{
                list-style-type: none;
                padding: 3.5rem .5rem;
                &:hover{
                    border-bottom: 5px solid $secondary;
                }

            }
            a {
                list-style-type: none;
                text-decoration: none;
                font-weight: 600;
                color: black;
                margin: 3px;
                padding: 3.5rem .5rem;
                &:active,
                &.active{
                color: $secondary;
                }
               
            }
        }
    }
}
</style>
