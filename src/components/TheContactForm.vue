<template>
  <section class="container contact">
    <div>

      <p> +48 000 000 000</p>
      <p> Street 1, 00-000 City</p>
    </div>
    <div>
      <form class="contact__form">
        <input
          type="text"
          placeholder="Imię"
          v-model="name"
          class="contact__form-input"
        />
        <input
          type="email"
          placeholder="Email"
          v-model="email"
          class="contact__form-input"
        />
        <textarea
          placeholder="Wiadomość"
          v-model="message"
          class="contact__form-input"
        ></textarea>
        <button type="submit" class="contact__form-button">Wyślij</button>
      </form>
    </div>
  </section>
</template>

<script setup lang="ts">

import { ref } from "vue";
const name = ref("");
const email = ref("");
const message = ref("");

/// ToDo use email js


</script>

<style scoped lang="scss">
.contact {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  margin: 0 auto;
  max-width: 1200px;
  margin-top: 100px;
}
.contact__form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  margin: 0 auto;
   .contact__form-input {
    width: 100%;
    margin: 10px 0;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}
</style>