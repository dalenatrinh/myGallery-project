<script setup>

const imagesData = [
  new URL('../assets/flower-sun.jpg',import.meta.url).href,
  new URL('../assets/hands-up.jpg',import.meta.url).href,
  new URL('../assets/ice-berg.jpg',import.meta.url).href,
  new URL('../assets/man-in-sand.jpg',import.meta.url).href,
  new URL('../assets/more-sand.jpg',import.meta.url).href,
  new URL('../assets/walking-on-rock.jpg',import.meta.url).href,
];

// Coloring heart with double click
let isHeartFilled = false;
// Toggle heart click
function handleHeartClick() {
    if(isHeartFilled = false) {
        isHeartFilled.style.fill = 'red';
        isHeartFilled = true;
        isHeartFilled = !isHeartFilled;
        
    } else {
        alert("error")
    }

};


</script>


<template>
    <div class="artContainer">
        <div v-for="img in imagesData" class="imageContainer">
        <img :src="img" class="images">
        <img :style="{filter: filterStyle}" src="../assets/heart.svg" class="heart" @dblclick="handleHeartClick()">
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
