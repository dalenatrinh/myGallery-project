<script setup>



</script>

<template>
    <div class="artContainer">
        <div class="imageContainer">
            <img class="heart" src="../assets/heart.svg">
            <img src="../assets/flower-sun.jpg" class="images">
        </div>
        <div class="imageContainer">
            <img class="heart" src="../assets/heart.svg">
            <img src="../assets/hands-up.jpg" class="images">
        </div>
        <div class="imageContainer">
            <img class="heart" src="../assets/heart.svg">
            <img src="../assets/man-in-sand.jpg" class="images">
        </div>
        <div class="imageContainer">
            <img class="heart" src="../assets/heart.svg">
            <img src="../assets/more-sand.jpg" class="images">
        </div>
        <div class="imageContainer">
            <img class="heart" src="../assets/heart.svg">
            <img src="../assets/walking-on-rock.jpg" class="images">
        </div>
        <div class="imageContainer">
            <img class="heart" src="../assets/heart.svg">
            <img src="../assets/ice-berg.jpg" class="images">
        </div>
    </div>
</template>

<style>
.artContainer {
    display: grid;
    justify-content: center;
    grid-template-columns: repeat(3, 400px);
    gap: 50px;
}

.imageContainer {
    position: relative;
}

.images {
    width: 25em;
    height: 20em;
    object-fit: cover;
}

.heart {
    position: absolute;
    width: 45px;
    top: 80%;
    left: 85%;
    filter: invert(100%) sepia(0%) saturate(0%) hue-rotate(253deg) brightness(105%) contrast(101%);
}
</style>
