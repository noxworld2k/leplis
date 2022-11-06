<script setup lang="ts">

import TheHeader from "@/components/TheHeader.vue";
import TheMainBanner from "@/components/TheMainBanner.vue";
import TheContent from "@/components/TheContent.vue";
import TheAboutUs from "@/components/TheAboutUs.vue";

</script>

<template>
  <TheHeader />
  <TheMainBanner />
  <TheContent />
  <TheAboutUs />
</template>

<style lang="scss">
.container__full-width {
    width: 100%;
    height: 100%;
    background-color: #000;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 0 20px;
}
.container {
  @media (max-width: 1200px) {
    width: 100%;
    margin: 0 auto;
    padding: 0 20px;
  }
    margin: 0 auto;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    width: 1200px;
    height: 100%;
    padding: 0 20px;
    box-sizing: border-box;
    font-family: 'Roboto', sans-serif;
    color: #333;
    font-size: 14px;
    line-height: 1.5;
    text-align: center;
}
</style>