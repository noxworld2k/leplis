<template>
  <section class="max">
    <div class="contact">
      <div class="contact__form">
        <iframe width="100%" height="300" frameborder="0" scrolling="no" marginheight="0" marginwidth="0" src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=en&amp;q=Kik%C3%B3%C5%82+(Leplis)&amp;t=&amp;z=13&amp;ie=UTF8&amp;iwloc=B&amp;output=embed"></iframe>
        <p><img class="phone-icon" src="@/assets/icons/phone.svg" alt="icon"> +48 000 000 000</p>
        <p><img class="phone-icon" src="@/assets/icons/pin.svg" alt="icon"> Street 1, 00-000 City</p>
      </div>
      <div>
        <h2 class="contact__title">
          Skontaktuj się z nami
        </h2>
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
  align-items: flex-start;
  padding: 0 20px;
  max-width: 1200px;
  margin: 100px auto 0;
}
.contact__form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 500px;
  margin: 0 auto;
  padding: 15px;

  .contact__form-input {
    width: 100%;
    margin: 10px 0;
    padding: 10px;
    border:none;
    border-bottom: 1px solid #000;
    &:focus {
      outline: none;
    }
    &::placeholder {
      color: rgb(158, 162, 162);
    }
  }
  p {
    display: flex;
    align-items: center;
    margin: 10px 0;
  }
  button {
    font-size: 1.2rem;
    width: 100%;
    margin: 10px 0;
    padding: 10px;
    border-radius: 5px;
    border: none;
    background-color: #8ddcdb;
    cursor: pointer;
    transition: all 0.3s ease-in-out;
    &:hover {
      background-color: #027b65;
      color: #fff;
    }
  }
}
.contact__title {
  text-align: center;
  text-transform: uppercase;
  margin: 10px 0;
}
.max {
  width: 100%;
  height: 100%;
  background-color: #ffffff;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 0 20px;
}
.phone-icon {
  width: 30px;
}

</style>