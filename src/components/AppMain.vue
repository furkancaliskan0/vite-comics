<template>
    <section>
        <div class="main">
            <div class="card">
                <div v-for="(card, index) in mainCard" :key="index" class="card-propeties">
                    <img :src="card.img" :alt="'card ' + (index)">
                    <h6>{{ card.name }}</h6>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "AppMain",
    data() {
        return {
            mainCard: [
                {
                    img: "/img/buy-comics-digital-comics.png",
                    name: "DIGITAL COMICS",
                },
                {
                    img: "/img/buy-comics-merchandise.png",
                    name: "DC MERCHANDISE",
                },
                {
                    img: "/img/buy-comics-subscriptions.png",
                    name: "SUBSCRPTION",
                },
                {
                    img: "/img/buy-comics-shop-locator.png",
                    name: "COMIC SHOP LOCATOR",
                },
                {
                    img: "/img/buy-dc-power-visa.svg",
                    name: "DC POWER VISA",
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
section {
    background-color: #0282f9;
    height: 100px;
    .main {
        height: 100%;
        .content {
            width: 100%;
        }
        .card {
            width: 80%;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            .card-propeties {
                width: 50%;
                height: 50%;
                margin: 20px 0;
                display: flex;
                justify-content: center;
                align-items: center;
            }
            h5 {
                margin-left: 10px;
                text-transform: uppercase;
            }
            img {
                width: 45px;
                height: 50px;
            }
           
        }
    }
}
</style>