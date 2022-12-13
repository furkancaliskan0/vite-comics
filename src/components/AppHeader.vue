<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    name: "CHARACTERS",
                    url: "#",
                    tap: "true",
                },
                {
                    name: "COMICS",
                    url: "#",
                    tap: "false",
                },
                {
                    name: "MOVIES",
                    url: "#",
                    tap: "false",
                },
                {
                    name: "TV",
                    url: "#",
                    tap: "false",
                },
                {
                    name: "GAMES",
                    url: "#",
                    tap: "false",
                },
                {
                    name: "COLLECTIBLES",
                    url: "#",
                    tap: "false",
                },
                {
                    name: "VIDEOS",
                    url: "#",
                    tap: "false",
                },
                {
                    name: "FANS",
                    url: "#",
                    tap: "false",
                },
                {
                    name: "NEWS",
                    url: "#",
                    tap: "false",
                },
                {
                    name: "SHOP",
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
        <div class="index-header">
            <nav>
                <div class="dc-logo">
                    <a href="#">
                        <img src="/img/dc-logo.png" alt="Dc-logo">
                    </a>
                </div>
                <li v-for="(link, index) in links" :key="index">
                        <a :class="{ active: links.tap }" :href="link.url">
                            {{ link.name }}
                        </a>
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
    .index-header {
        width: 100%;
        margin: 0 auto;
        nav {
            display: flex;
            justify-content: center;
            align-items: center;
            .dc-logo {
                text-align: center;
                width: 40%;
            }
            li{
                list-style-type: none;
                text-decoration: none;
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
