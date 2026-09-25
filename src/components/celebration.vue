<script lang="ts" setup>
import meowy from '../assets/meowy-birthday.png'
import Heart from '../components/heart.vue';
import Drool from './drool.vue';

function randomDegree(): number {
    const rand = Math.floor(Math.random() * 80);
    return rand < 10 ? 50 : rand;
}

function randomHorizontal() {
    const rand = Math.floor((Math.random() * 15))
    return rand < 10 ? 10 : rand;
}

</script>
<template>
    <div class="main-container" , id="main">

        <p class="birthday-title">HAPPY BIRTHDAY MEOWYYYYY!!! <Drool class="drool"></Drool>
        </p>
        <img :src="meowy" alt="meowy" class="meowy">
        <p class="birthday-text">i love you lots!!!! i wish you the best birthday today you deserve all the love in the
            world</p>
        <marquee behavior="alternate" direction="right" class="yay">
            <p>YAAAAAAAAY</p>
        </marquee>
        <Heart v-bind:style="{
            transform: `rotate(${randomDegree() - 10}deg)`,
            top: '10%',
            left: `${randomHorizontal()}%`

        }"></Heart>
        <Heart v-bind:style="{
            transform: `rotate(-${randomDegree()}deg)`,
            top: '25%',
            right: `${randomHorizontal()}%`
        }"></Heart>
        <Heart v-bind:style="{
            transform: `rotate(${randomDegree()}deg)`,
            top: '35%',
            left: `${randomHorizontal()}%`
        }"></Heart>
        <Heart v-bind:style="{
            transform: `rotate(-${randomDegree()}deg)`,
            top: '50%',
            right: `${randomHorizontal()}%`
        }"></Heart>
        <Heart v-bind:style="{
            transform: `rotate(${randomDegree()}deg)`,
            top: '60%',
            left: `${randomHorizontal()}%`
        }"></Heart>
        <Heart v-bind:style="{
            transform: `rotate(-${randomDegree()}deg)`,
            top: '75%',
            right: `${randomHorizontal()}%`
        }"></Heart>
    </div>
</template>
<style scoped>
.main-container {
    min-height: 100vh;
    background: linear-gradient(180deg, #e994ff, #fac7ff);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
    text-align: center;
    position: relative;
    color: #fff7e8;
}

.birthday-title {
    font-size: calc(2.7rem + 0.390625vw);
    z-index: 1;
    font-weight: 900;
    position: relative;
    background-color: #d866ff;
    padding: 10px 20px;
    border-radius: 20px;
    margin: 0 20px;
}

.meowy {
    width: clamp(200px, 20%, 450px);
    border-radius: 50%;
    box-shadow: 1px 1px 30px #d857f8;
}

.birthday-text {
    font-size: calc(20px + 0.390625vw);
    width: 35ch;
    text-align: center;
    z-index: 1;
    font-weight: 600;
    background-color: #f0a4fc;
    padding: 10px 20px;
    border-radius: 20px;
    margin: 0 20px;
}

.yay {
    position: absolute;
    top: 20px;
    z-index: 1;
    font-size: calc(2rem + 0.390625vw);

    & p {
        padding: 10px;
        background-color: #d866ff;
        width: fit-content;
        border-radius: 10px;
    }
}

.drool {
    position: absolute;
    width: 100px;
    top: -80px;
    right: 0;
    z-index: 4;
}
</style>