<script></script>

<template>

    <div class="series">
        <div class="square">
            <img src="../../assets/img/footer-bg.jpg" alt="img">

                <div>ACTION COMICS</div>
                
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
                
        img {
            height: 80%;
            width: 100%;
            object-fit: cover;
            margin-bottom: .8rem;
        }
    }
}

// debug
.square {
    height: 100px;
    background-color: turquoise;
    border: 1px solid black;
}


</style>