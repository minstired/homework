<script setup>
// import { reactive } from 'vue';

const whyUsIMG = './public/whyUs.svg'

const cardFst = {
    header: 'Trustworthy partnership',
    content: '20+ successfully executed projects in Southeast Asia, South America, Eastern Europe and the CIS Region.'
};

const cardScnd = {
    header: 'Our Team',
    content: 'ANTEI leverages a global team of 20+ seasoned experts across diverse disciplines, from business analysis and technological to marketing and physical execution. This comprehensive team ensures prompt execution of projects from different industries and business regions.'
}

</script>

<template>
    <section id="WhyUs">
        <h2>Why Us?</h2>
        <div class="cardsContainer">
            <div id="whyUsContainer"><img :src="whyUsIMG" alt="Our Team Image"></div>
            <div id="cardFst" class="whyUsCard">
                <div class="cardHeader">{{ cardFst.header }}</div>
                <p> {{ cardFst.content }}</p>
            </div>
            <div id="cardScnd" class="whyUsCard">
                <div class="cardHeader">{{ cardScnd.header }}</div>
                <p> {{ cardScnd.content }}</p>
            </div>
        </div>
    </section>.
</template>

<style scoped lang="scss">
section {
    margin: 5% 20%;
    height: auto;

    h2 {
        text-align: center;
        font-size: 2rem;
        margin-bottom: 2rem;
        color: #FFC107;
        font-style: italic;
        font-weight: 900;
    }

    .cardsContainer {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 5%;
        // height: max-content;
        align-items: center;


        #whyUsContainer {
            height: 500px;
            width: 500px;
            position: relative;
            overflow: hidden;

            img {
                position: absolute;
                height: 180%;

                top: -200px;
                right: -200px;
            }
        }

        .whyUsCard {
            height: fit-content;

            div.cardHeader {

                text-align: center;
                align-items: center;

                font-size: 2rem;
                font-weight: 800;
                margin-bottom: 1rem;

            }

            p {
                font-size: 1.5rem;
                line-height: 2.4rem;
                opacity: 0.8;
                
            }
        }

        #cardScnd {
            grid-column-start: span 2;
        }
    }
}
</style>