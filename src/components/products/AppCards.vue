<script>

    export default {
        props : {
            comics : Array,
        }
    }

</script>

<template>

    <div class="series">
        <div class="square"  v-for="comic in comics" :key="comic.thumb">

            <div class="card-container">

                <!-- <img src="../../assets/img/footer-bg.jpg" alt="img"> -->
                <img :src="comic.thumb" alt="">

                <!-- <div>ACTION COMICS</div> -->
                <div>{{ comic.series }}</div>

            </div>
            
        </div>
    </div>


</template> 

<style lang="scss" scoped>

.series {
    min-height: 10rem;

    display: flex;
    flex-wrap: wrap;

    .square {
        width: calc(100% / 6);
        height: 250px;
        margin: 1.5rem 0;
        padding: 0 .5rem 0 .5rem;
                
        .card-container {
            height: 100%;
            width: 100%;

            img {
                height: 80%;
                width: 100%;
                // object-fit: cover;
                margin-bottom: .8rem;
            }
        }
    }
}


</style>