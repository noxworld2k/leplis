<template>
  <section class="container-fullwidth">
    <div class="container">
      <img class="content__image-main" src="/img/music.png" alt="logo"/>
    </div>
    <div class="container container__offer">
      <div v-for="offer in offerData" class="content__offer">
        <img class="content__image" :src="offer.image" alt="logo"/>
        <div class="content__offer-textbox">
          <h3 class="content__title">{{ offer.title }}</h3>
          <p class="content__text">{{ offer.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import offers from "@/data/data.json";

const offerData = offers.offers;


</script>

<style scoped>
.content__image-main {
  margin: 50px auto 0;
  max-width: 600px;
  min-width: 300px;
}
.container__offer {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  object-fit: cover;
  object-position: center;
  margin: 2rem auto;
}

.content__offer {
  display: flex;
  flex-direction: row;
  width: 500px;
  margin: 2rem auto;
  padding: 1rem;
  border-radius: 5px;
}

.content__image {
  height: 200px;
  width: 200px;
  object-fit: cover;
  object-position: center;
  margin: 2rem auto;
  border-radius: 50%;
}

.content__title {
  margin: 1rem auto;
  font-size: 1.5rem;
  font-weight: 700;
}

.content__text {
  margin: 1rem auto;
  font-size: 1rem;
  font-weight: 400;
}
.content__offer-textbox {
  font-size: 1rem;
  font-weight: 400;
  padding: 1rem;
}
</style>