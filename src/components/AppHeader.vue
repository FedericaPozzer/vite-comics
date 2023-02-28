<script>

export default {
    data() {
        return {
            headerMenu: [
                {
                    name: "CHARACTERS",
                    status: "active",
                    link: ""
                },
                {
                    name: "COMICS",
                    status: "",
                    link: ""
                },
                {
                    name: "MOVIES",
                    status: "",
                    link: ""
                },
                {
                    name: "TV",
                    status: "",
                    link: ""
                },
                {
                    name: "GAMES",
                    status: "",
                    link: ""
                },
                {
                    name: "COLLECTIBLES",
                    status: "",
                    link: ""
                },
                {
                    name: "VIDEOS",
                    status: "",
                    link: ""
                },
                {
                    name: "FANS",
                    status: "",
                    link: ""
                },
                {
                    name: "NEWS",
                    status: "",
                    link: ""
                },
                {
                    name: "SHOP",
                    status: "",
                    link: ""
                },
            ]
        }
    }
}

</script>

<template>
    <section>
        <div class="header-bar container">
            <div class="img-container">
                <img src="../assets/img/dc-logo.png" alt="logo">
            </div>

            <div>
                <ul>
                    <li v-for="(element, index) of headerMenu" v-bind:key="element.name">
                        <a href="#"> {{ element.name }} </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
/* debug */
section {
    /* margin-top: 20rem;
         */
    background-color: #ffffff;
    padding: 2rem 0 2rem 0;
}

.header-bar {
    display: flex;
    align-items: center;
    justify-content: space-between;

    height: 5rem;
}

.img-container {
    height: 5rem;
}

ul {
    display: flex;
}

ul li {
    margin-left: 2rem
}
</style>
