<template>
  <header class="container__full-width">
    <div class="container">
      <div>
        <img class="header__logo" src="/img/logo.png" alt="logo zespołu leplis" />
      </div>
      <div>
        <ul class="header__nav">
          <li>
            <router-link to="/">Strona Główna</router-link>
          </li>
          <li>
            <router-link to="/utworz-playliste">Utwórz własną playlistę</router-link>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
.header__logo {
  width: 250px;
}
.header__nav {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
  a {
    line-height: 1.5;
    text-decoration: none;
    color: #ffffff;
    padding: 0 20px;
    text-transform: uppercase;
    font-size: 1.2rem;
    &:hover {
      color: #5eb9dd;
    }
  }
}
</style>