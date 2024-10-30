<script setup>
import { reactive } from 'vue';

const cards = reactive([
    {
        header: 'Document Summarization & Info Extraction',
        content: 'Summarization and extract from huge documents and books with a single API call. Our custom chunking and extraction pipelines are capable of returning results specific to your need.'
    },  {
        header: 'Improve Product Capabilities',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. A modi nostrum libero at sed saepe laborum quos magni ad? Ducimus perspiciatis asperiores sint eum totam obcaecati. Provident rerum sequi consequuntur.'
    
    },  {
        header: 'Other',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. A modi nostrum libero at sed saepe laborum quos magni ad? Ducimus perspiciatis asperiores sint eum totam obcaecati. Provident rerum sequi consequuntur.'
    },
]);
</script>

<template>
    <section id="WhyAI">
        <h2>How does AI&ML help your buisness</h2>
        <div class="cardsContainer">
            <div v-for="card in cards" class="AICard">
                <div class="cardHeader">{{ card.header }}</div>
                <p> {{ card.content }}</p>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
section {
    margin: 0% 9%;
    h2 {
        text-align: center;
        font-size: 2rem;
        margin-bottom: 4rem;
    }
    .cardsContainer {
        display: flex;
        justify-content: space-evenly;
        height: max-content;

        .AICard {
            width: 25%;
            background-color: rgb(14, 14, 14);
            padding: 2%;
            padding-top: 3%;

            div.cardHeader {
                
                text-align: center;
                align-items: center;

                font-size: 1.5rem;
                font-weight: 800;
                height: 6rem;
            }
            p {
                font-size: 1.3rem;
                line-height: 1.8rem;
                opacity: 0.8;
            }

            
        }
    }
}
</style>