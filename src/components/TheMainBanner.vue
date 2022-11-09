<template>
  <section class="container__fullwidth banner__main">
    <div class="banner__main-content">
      <h1 class="banner__main__title">
        Zespół muzyczny Leplis
      </h1>
      <p class="banner__main__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed euismod, nisl nec
        aliquam aliquam, nunc nisl aliquet nisl, eget aliquam nisl nisl sit amet lorem. Sed euismod, nisl nec aliquam
        aliquam, nunc nisl aliquet nisl, eget aliquam nisl nisl sit amet lorem.</p>
    </div>
  </section>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
.banner__main {
  background-image: url(/img/baner_2.png);
  height: 90vh;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  display: flex;
  align-items: center;
  justify-content: flex-end;
}

.banner__main__title {
  font-size: 3rem;
  font-weight: 700;
  color: #fff;
  text-transform: uppercase;
  margin-bottom: 30px;
  text-align: center;
}

.banner__main__text {
  font-size: 1rem;
  font-weight: 400;
  color: #fff;
  text-transform: uppercase;
}

.banner__main-content {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  width: 600px;
  //background-color: rgba(0, 0, 0, 0.5);
  padding: 25px;
  margin-right: 15%;
  border-radius: 10px;
}

</style>