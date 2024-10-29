<script setup>

const logoIMG = './public/Logo.webp'
const mainPageUrl = 'https://anteihk.com'
const navbar = ['About us', 'Partners', 'Contact']
const burgerSVG = '/burgerMenu.svg'

</script>

<template>
    <header>
        <a :href="mainPageUrl" id="logoLink"><img :src="logoIMG" alt="anteink logo"></a>
        <nav>
            <button class="mobile-burger-toggle">
                <img :src="burgerSVG" alt="burger toggle">
            </button>
            <ul>
                <li v-for='section in navbar' :key="section" :href="'#' + section">{{ section }}</li>
            </ul>
        </nav>
    </header>
</template>

<style scoped lang="scss">
header {
    height: 10vh;
    padding: 1% 15%;

    display: flex;
    align-items: center;
    justify-content: space-between;

    font-weight: 600;
    font-size: 1.1rem;

    a#logoLink {
        height: 100%;
        display: flex;
    }

    img {
        height: 80%;
        align-self: center;
    }

    nav {
        // width: fit-content;
        ul {
            list-style: none;
            display: flex;
            gap: 2.5rem;

            padding: 0;
            margin: 0;

            li {
                white-space: nowrap;
                
            }

            li:hover {
                color: #FFC107;
            }
        }

        button {
            height: 50%;
            background-color: black;
            display: none;
        }
    }
}
</style>