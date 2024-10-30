<script setup>
import { reactive } from 'vue';

const logos = reactive([{
    name: 'Deloitte',
    src: '/Deloitte.svg',
}, {
    name: 'Cybersport',
    src: '/Cyberport.png',
}, {
    name: 'InvestHK',
    src: '/InvestHK.svg',
}, {
    name: 'AWS',
    src: '/AWS.svg',
}, {
    name: 'ITMO',
    src: '/ITMO.svg',
}, {
    name: 'HKSTP',
    src: '/HKSTP.png',
}, {
    name: 'UST',
    src: '/UST.svg',
}, {
    name: 'SparkusTech',
    src: '/Sparkus.svg',
}])

</script>

<template>
    <section id="Partners">
        <h2>Our partners</h2>
        <div class="cardsContainer">
            <div v-for="logo in logos" class="imgContainer">
                <img :id="logo.name" :src="logo.src" :alt="logo.name">
            </div>
        </div>
        <h3> Among many others.</h3>
    </section>
</template>

<style scoped lang="scss">
section {
    margin: 0% 15%;
    margin-bottom: 5%;
    height: auto;

    h2 {
        text-align: center;
        font-size: 2rem;
        margin-bottom: 5rem;
        font-weight: 900;
    }

    .cardsContainer {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 2rem;
        row-gap: 1.5rem;
        grid-template-rows: repeat(2, 1fr);

        .imgContainer {
            height: 90%;
            width: 100%;
            overflow: hidden;
            background-color: white;
            color: black;
            display: flex;
            justify-content: center;
            border-radius: 1rem;

            img {
                width: 80%;
                align-self: center;
                padding: 0.5rem;
            }

            #UST {
                    width: 20%;
                }
        } 
    }
    h3 {
        text-align: center; 
        margin-top: 2rem;
        font-weight: 700;
    }
}
</style>