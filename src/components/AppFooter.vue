<script>
export default {
    data() {
        return {
            footerIcons : [
                "footer-facebook.png",
                "footer-twitter.png",
                "footer-youtube.png",
                "footer-pinterest.png",
                "footer-periscope.png",
            ]
        }
    },

    methods : {
        getIconPath : function(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="bg">
        <section class="container footer">
            <div class="links">
                <div>
                    <div class="lista">
                        <h2>DC COMICS</h2>
                        <ul>
                            <li><a href="#">Characters</a></li>
                            <li><a href="#">Comics</a></li>
                            <li><a href="#">Movies</a></li>
                            <li><a href="#">TV</a></li>
                            <li><a href="#">Games</a></li>
                            <li><a href="#">Videos</a></li>
                            <li><a href="#">News</a></li>
                        </ul>
                    </div>
                    <div class="lista">
                        <h2>SHOP</h2>
                        <ul>
                            <li><a href="#">Shop DC</a></li>
                            <li><a href="#">Shop DC Collectibles</a></li>
                        </ul>
                    </div>
                </div>
                <div class="lista">
                    <h2>DC</h2>
                    <ul>
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy Policy (new)</a></li>
                        <li><a href="#">Add Choices</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                </div>
                <div class="lista">
                    <h2>SITES</h2>
                    <ul>
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>

                </ul>
                </div>

            </div>

            <div class="logo-big">
                <img src="../assets/img/dc-logo-bg.png" alt="logoBig">
            </div>

        </section>
    </div>

    <div class="footer-footer">
        <div class="container">
            <div>
                <button>SIGN-UP NOW!</button>
            </div>

            <div class="footer-icons">
                <h2>FOLLOW US</h2>
                <div v-for="(icon, i) in footerIcons">
                    <img :src="getIconPath(footerIcons[i])" alt="icon">
                </div>
                <!-- <a href="#"><img src="../assets/img/footer-facebook.png" alt="icon"></a>
                <a href="#"><img src="../assets/img/footer-twitter.png" alt="icon"></a>
                <a href="#"><img src="../assets/img/footer-youtube.png" alt="icon"></a>
                <a href="#"><img src="../assets/img/footer-pinterest.png" alt="icon"></a>
                <a href="#"><img src="../assets/img/footer-periscope.png" alt="icon"></a> -->
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.bg {
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height: 28rem;
    overflow: hidden;
}

.footer h2 {
    margin-bottom: .5rem;
}

.footer {
    display: flex;
    justify-content: space-between;
}

.links {
    color: white;
    display: flex;
    padding-top: 2rem;
}

.lista {
    padding: 1rem;
}

.lista li {
    font-size: .8rem;
    color: grey;
}

.logo-big {
    margin-top: -3rem;
}

.footer-footer {
    background-color: #303030;
    padding: 2rem;
}

.footer-footer .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

button {
    background-color: inherit;
    border: 1px solid #0282f9;
    padding: .8rem;
    font-size: .9rem;
    color: white;
    cursor: pointer;
}

.footer-footer h2 {
    color: #0282f9;
    margin-right: 1rem;
}

.footer-icons {
    display: flex;
    align-items: center;
    cursor: pointer;
}

.footer-icons img {
    margin-left: 1rem;
}
</style>
