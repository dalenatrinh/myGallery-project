<script setup>
import galleryNav from './components/GalleryNav.vue'
import ArtGallery from './components/ArtGallery.vue'
</script>

<template>
  <div class="nav">
    <img src="./assets/user.jpg" class="profile" alt="Online icon" />
    <div>
      <p>yourName</p>
      <p class="status">Online </p>
    </div>

  </div>
  <div class="galleryContent">
    <div>
      <galleryNav />
      <div class="line"></div>
    </div>
  </div>

  <div class="artGallery">
    <ArtGallery />
  </div>
</template>

<style scoped>
.profile {
  width: 70px;
  height: 70px;
  padding: 0.5em;
  border-radius: 50%;
  object-fit: cover;
}

.nav {
  display: flex;
  align-items: center;

}

.status {
  color: green;
  font-weight: 400;
}

.galleryContent {
  display: flex;
  justify-content: center;
}

.line {
  height: 1px;
  width: 50em;
  background-color: black;
}

.artGallery {
  margin-top: 50px;
}
</style>
