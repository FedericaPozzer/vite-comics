<script>
import AppCards from "./products/AppCards.vue"

export default {
    components : {AppCards},

    data() {
        return {
            links : [
                {
                    icon : "buy-comics-digital-comics.png",
                    name : "DIGITAL COMICS",
                    number : 0,
                },
                {
                    icon : "buy-comics-merchandise.png",
                    name : "DC MERCHANDISE",
                    number: 1,
                },
                {
                    icon : "buy-comics-subscriptions.png",
                    name : "SUBSCRIPTION",
                    number : 2,
                },
                {
                    icon : "buy-comics-shop-locator.png",
                    name : "COMIC SHOP LOCATOR",
                    number : 3,
                },
                {
                    icon : "buy-dc-power-visa.svg",
                    name : "DC POWER VISA",
                    number : 4,
                },
            ]
        }
    },

    methods : {
        getImagePath: function(img) {
            // return new URL(`${img}`, import.meta.url).href; --not working
            // return new URL("../assets/img/buy-comics-digital-comics.png", import.meta.url).href; --that's why!
            // return new URL("../assets/img/" + img, import.meta.url).href; --one right option (another right option below)
            return new URL(`../assets/img/${img}`, import.meta.url).href;

        }
    }
}
</script>

<template>
    <section class="section-content">
        <div class="jumbotron">
            <img src="../assets/img/jumbotron.jpg" alt="jumbo">
        </div>

        <div class="container section-series">
            <h3>CURRENT SERIES</h3>

            <AppCards></AppCards>

            <div class="btndiv">
                <button>LOAD MORE</button>
            </div>
        </div>

    </section>

     <section class="section-links">
        <ul class="container">
             <li v-for="link of links" v-bind:key="link.number">
                <img :src="getImagePath(link.icon)" alt="icon">
                <a href="#"> {{ link.name }} </a>
            </li>

            <!-- <li>
                <img src="../assets/img/buy-comics-digital-comics.png" alt="icon">
                <div>DIGITAL COMICS</div> 
            </li>

            <li>
                <img src="../assets/img/buy-comics-merchandise.png" alt="icon">
                <div>DC MERCHANDISE</div>
            </li>

            <li>
                <img src="../assets/img/buy-comics-subscriptions.png" alt="icon">
                <div>SUBSCRIPTION</div>
            </li>

            <li>
                <img src="../assets/img/buy-comics-shop-locator.png" alt="icon">
                <div>COMIC SHOP LOCATOR</div>
            </li>

            <li>
                <img src="../assets/img/buy-dc-power-visa.svg" alt="icon" class="icon-smaller">
                <div>DC POWER VISA</div>
            </li> -->
            
        </ul>
    </section>
</template>

<style lang="scss" scoped>
.section-content {
    background-color: #1c1c1c;
    color: #ffffff;

    .jumbotron {
        max-height: 23rem;
        overflow: hidden;
        img {
            max-width: 100%;
        }
    }

    .section-series {
        min-height: 30rem;
        background-color: pink;
        

        h3 {
            background-color: #0282f9;
            border: 1px solid #0282f9;
            padding: .8rem;
            font-size: 1rem;
            color: white;
            cursor: pointer;
            display: inline;

            margin-top: -2rem;
        }
    
        .btndiv {
            display: flex;

            button {
                background-color: #0282f9;
                border: 1px solid #0282f9;
                padding: .5rem 2rem;
                font-size: .9rem;
                color: white;
                cursor: pointer;
            }
        }

        

    }
   
}

.section-links {
    background-color: #0282f9;

    ul {
        display: flex;
        justify-content: space-between;
        padding: 4rem 0; 

        li {
            display: flex;
            align-items: center;
            max-width: calc(100% / 5);
            cursor: pointer;

            img {
                max-height: 3rem;
            }

            a {
                color: #ffffff;
                font-size: .9rem;
                margin-left: .8rem;
            }
        }
    }
}

// ul:last-child img {
//     height: 1.8rem;
// }
</style>
