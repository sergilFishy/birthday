<script lang="ts"></script>
<template>
    <div class="heart"></div>
</template>
<style scoped>
.heart {
    width: 100px;
    height: 100px;
    background: linear-gradient(0deg, #f8a9ff, #d35bff);
    clip-path: path('M50 90 C25 70, 0 50, 0 30 C0 10, 20 0, 35 0 C45 0, 50 10, 50 20 C50 10, 55 0, 65 0 C80 0, 100 10, 100 30 C100 50, 75 70, 50 90Z');
    --heart-size: clamp(50px, 4vw, 100px);
    transform: scale(4);
    position: absolute;
}


/* .heart,
.heart::after,
.heart::before {
    background: linear-gradient(0deg, #fac7ff, #dc7dff);
    background-repeat: no-repeat;
    background-size: calc(var(--heart-size) * 1.5) calc(var(--heart-size) * 1.5);
}

.heart::after {
    content: "";
    height: var(--heart-size);
    width: var(--heart-size);
    border-radius: 50%;
    background-position: 0 0;
    position: absolute;
    top: calc((var(--heart-size) / 2) * -1);
    left: 0;
}

.heart::before {
    position: absolute;
    content: "";
    width: var(--heart-size);
    border-radius: 50%;
    height: var(--heart-size);
    left: calc(var(--heart-size) / 2);
    background-position: calc(var(--heart-size) * -0.5) calc(var(--heart-size) * -0.5);
} */
</style>