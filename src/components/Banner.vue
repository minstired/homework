<script setup>
const bannerIMG = './public/bannerSVG.svg'
</script>

<template>
    <section id="Banner">
        <div id="leftBannerSide">
            <img :src="bannerIMG" alt="Banner Image">
        </div>
        <div id="rightBannerSide">
            <h1 id="accentColor">AI and Machine Learning</h1>
            <h1>Consulting Services</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. A modi nostrum libero at sed saepe laborum quos
                magni ad? Ducimus perspiciatis asperiores sint eum totam obcaecati. Provident rerum sequi consequuntur.
            </p>
        </div>

    </section>
</template>

<style scoped lang="scss">
section {
    height: 30%;
    display: flex;
    justify-content: space-evenly;
    margin: 5% 15%;

    #leftBannerSide {
        height: 550px;
        width: 600px;
        position: relative;
        overflow: hidden;

        img {
            position: absolute;
            height: 200%;

            top: -300px;
            right: -250px;
        }
    }

    #rightBannerSide {
        width: 40%;

        h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
        }

        p {
            margin-top: 2.5rem;
            font-size: 1.5rem;
            opacity: 0.8;
        }
    }
}

#accentColor {
    color: #FFC107;
    font-weight: 800;
}
</style>