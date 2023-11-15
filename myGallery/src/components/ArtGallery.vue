<script setup>
import {ref} from 'vue';

// Billeder
const imagesData = [
  new URL('../assets/flower-sun.jpg',import.meta.url).href,
  new URL('../assets/hands-up.jpg',import.meta.url).href,
  new URL('../assets/ice-berg.jpg',import.meta.url).href,
  new URL('../assets/man-in-sand.jpg',import.meta.url).href,
  new URL('../assets/more-sand.jpg',import.meta.url).href,
  new URL('../assets/walking-on-rock.jpg',import.meta.url).href,
];

// Object to track the double click state for each image
const imageDoubleClickState = imagesData.map(() => ref(false));


const toggleHeart = (index) => {
  // Toggle the double click state for the clicked image
  imageDoubleClickState[index].value = !imageDoubleClickState[index].value;
};


</script>


<template>
    <div class="artContainer">
      <div v-for="(img, index) in imagesData" :key="index" class="imageContainer">
        <img :src="img" class="images">
        <img
        :class="{'red-filter': imageDoubleClickState[index].value, 'no-filter': !imageDoubleClickState[index].value}"
        src="../assets/heart.svg"
        class="heart"
        @dblclick="() => toggleHeart(index)"
/>
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
   
}

.red-filter {
    filter: invert(43%) sepia(99%) saturate(5996%) hue-rotate(348deg) brightness(98%) contrast(89%);
}

.no-filter {
    filter: invert(100%) sepia(0%) saturate(0%) hue-rotate(253deg) brightness(105%) contrast(101%);
}
</style>
