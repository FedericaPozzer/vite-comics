<script>
export default {
    // data() {
    //     return {
    //         links : [
    //             {
    //                 icon : "../assets/img/buy-comics-digital-comics.png",
    //                 name : "DIGITAL COMICS",
    //             },
    //             {
    //                 icon : "../assets/img/buy-comics-digital-comics.png",
    //                 name : "DC MERCHANDISE",
    //             },
    //             {
    //                 icon : "../assets/img/buy-comics-digital-comics.png",
    //                 name : "SUBSCRIPTION",
    //             },
    //             {
    //                 icon : "../assets/img/buy-comics-digital-comics.png",
    //                 name : "COMIC SHOP LOCATOR",
    //             },
    //             {
    //                 icon : "../assets/img/buy-comics-digital-comics.png",
    //                 name : "DC POWER VISA",
    //             },
    //         ]
    //     }
    // },

    // methods : {
    //     getImagePath: function(img) {
    //         return new URL(`${img}`, import.meta.url).href;
    //     }
    // }
}
</script>

<template>
    <section class="section-content">
        <div class="container">
            <h2> --> Content goes here &lt;-- </h2>
        </div>

    </section>

     <section class="section-links">
        <ul class="container">
             <!-- <li v-for="(link, index) of links" v-bind:key="link.index">
                <img :src="getImagePath(link.icon)" alt="icon">
                <img src="../assets/img/buy-comics-digital-comics.png" alt="">
                <a href="#"> {{ link.name }} </a>
            </li> -->

            <li>
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
            </li>
            
        </ul>
    </section>
</template>

<style lang="scss" scoped>
.section-content {
    background-color: #1c1c1c;
    color: #ffffff;
}

h2 {
    padding: 4rem;
}

.section-links {
    background-color: #0282f9;
}

ul {
    display: flex;
    justify-content: space-between;
    padding: 4rem 0; 
}

ul li {
    display: flex;
    align-items: center;
    max-width: calc(100% / 5);
    cursor: pointer;
}

li div {
    color: #ffffff;
    font-size: .9rem;
}

ul img {
    max-height: 3rem;
}

.icon-smaller {
    height: 1.8rem;
}

ul div {
    margin-left: .8rem;
}
</style>
