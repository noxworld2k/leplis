<template>
<section>
  <div class="container ">
    <div class="youtube__box">
      <img src="/img/monitor.png" alt="monitor">
      <iframe class="youtube__video" width="560" height="315" src="https://www.youtube.com/embed/QhicWbN4egc&mute=1" title="!BEST! Oldschool Techno Hands Up Trance Jumpstyle Mix 2016" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
    <div class="contact__box">
      <h2 class="contanct__box-tiitle">
      Poznaj Nas
      </h2>
      <p class="contact__box-about">
        Sample text. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla quis lorem ut libero malesuada feugiat.Sample text. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla quis lorem ut libero malesuada feugiat.
      </p>

      <p class="contact__box-another">
        Sample text. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla quis lorem ut libero malesuada feugiat.
      </p>

      <p class="contact__box-tel">
      +48 123 456 789
      </p>

    </div>
  </div>
</section>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
.youtube__box {
  position: relative;
  width: 500px;
  img {
    width: 100%;
  }
  iframe {
    position: absolute;
    top: 15px;
    left: 19px;
    width: 463px;
    height: 300px;
  }
}
.contact__box {
  width: 500px;
  margin-left: 50px;
  color: #000000;
  text-align: left;
  .contanct__box-tiitle {
    font-size: 2rem;
    font-weight: 700;
    text-transform: uppercase;
    margin-bottom: 20px;
    border-bottom: #52dddb 5px solid;
  }
  .contact__box-about {
    font-size: 1rem;
    font-weight: 400;
    margin-bottom: 15px;
  }
  .contact__box-another {
    font-size: 1rem;
    font-weight: 800;
    margin-bottom: 15px;
  }
  .contact__box-tel {
    font-size: 2rem;
    font-weight: 700;
    text-transform: uppercase;
    margin-bottom: 0;
    color: #48c4c2;
  }
}

</style>