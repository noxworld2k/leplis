// @ts-nocheck
<template>
  <div class="container">
    <form class="form__box">
      <button
          class="btn__toggle"
          v-if="!playlistDone"
          @click.prevent="togglePlaylistDone"
      >
        Wybrałeś własne kawałki ?
      </button>
      <button class="btn__toggle" v-else @click.prevent="togglePlaylistDone">
        Wybierz playlistę
      </button>
      <div
          class="playlist"
          v-for="item in playListData"
          :key="item.title"
          v-if="!playlistDone"
      >
        <div class="playlist__item" @click="addSongToPlaylist">
          <input
              type="checkbox"
              :value="item.title"
              @click="addSongToPlaylist"
          />
          {{ item.title }} -
          <a class="button-link"
             :key="item.title"
             :href="`https://www.youtube.com/watch?v=${item.videoId}`"
             target="_blank"
          >Przesłuchaj kawałek
          </a>
        </div>
      </div>
      <div class="form__user-data" v-else>
        <label for="name">Imię</label>
        <input
            type="text"
            name="name"
            placeholder="Podaj swoję imię"
            v-model="userData.name"
            required
        />
        <label for="email">Email</label>
        <input
            type="email"
            name="email"
            placeholder="Podaj swój email"
            v-model="userData.email"
            required
        />
        <label for="date">Wybierz datę uroczystości</label>
        <input type="date" name="date" v-model="userData.date"/>
        <label for="message">Napisz nam czego oczekujesz</label>
        <textarea
            name="message"
            placeholder="Napisz nam czego oczekujesz"
            v-model="userData.message"
        ></textarea>
        <button class="btn__submit" @click.prevent="sendUserData">
          Wyślij
        </button>
      </div>
    </form>
  </div>
</template>

<script setup lang="ts">
import {onBeforeMount, ref, watchEffect} from "vue";

const ApiKey = "AIzaSyCNKSMO5i8RFdHYSIuuO0zVl0FCPPl5VfA";
const playListId = "PLWfiGYuvhOCv11AUOF-CC_fY7Hktfq4Cl";
const playListData = ref([]);

const fetchData = async () => {
  const response = await fetch(
      `https://youtube.googleapis.com/youtube/v3/playlistItems?part=snippet&maxResults=150&playlistId=${playListId}&key=${ApiKey}`
  );
  const data = await response.json();
  data.items.forEach((item: any) => {
    playListData.value.push({
      title: item.snippet.title,
      videoId: item.snippet.resourceId.videoId,
    });
  });
};
onBeforeMount(() => {
  fetchData();
});

const playlist = ref([]);

const addSongToPlaylist = (event: { target: { checked: any; value: any } }) => {
  if (event.target.checked) {
    playlist.value.push(event.target.value);
  } else {
    playlist.value = playlist.value.filter(
        (item: any) => item !== event.target.value
    );
  }
};
watchEffect(() => {
  console.log(playlist.value);
});

const userData = ref({
  name: "",
  message: "",
  date: "",
  email: "",
});
const playlistDone = ref(false);

const sendUserData = () => {
  console.log(userData.value);
};

const togglePlaylistDone = () => {
  playlistDone.value = !playlistDone.value;
};
</script>

<style scoped lang="scss">
.form__box {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  margin: 0 auto;
  width: 100%;
  max-width: 1200px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  background-color: #fff;

  .playlist {
    &:nth-child(odd) {
      background-color: #f5f5f5;
    }
    .playlist__item {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 1000px;
      padding: 10px;
      border-bottom: 1px solid #ccc;
    }
  }
}

.btn__toggle {
  padding: 10px;
  border: 1px solid #0031d4;
  border-radius: 5px;
  background-color: #0031d4;
  cursor: pointer;
  color: #fff;
  margin: 0 auto;

  &:hover {
    background-color: #041c6c;
  }
}

.form__user-data {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: center;
  margin: 0 auto;
  width: 100%;
  max-width: 1200px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  background-color: #fff;

  label {
    margin-bottom: 10px;
  }

  input {
    width: 300px;
    margin-bottom: 10px;
  }

  textarea {
    width: 300px;
    margin-bottom: 10px;
  }
}

.btn__submit {
  padding: 10px;
  border: 1px solid #0031d4;
  border-radius: 5px;
  background-color: #0031d4;
  cursor: pointer;
  color: #fff;
  margin: 0 auto;

  &:hover {
    background-color: #041c6c;
  }
}

.button-link {
  color: #fff;
  text-decoration: none;
  padding: 10px;
  background-color: #0031d4;

  &:hover {
    color: #041c6c;
  }
}
</style>
