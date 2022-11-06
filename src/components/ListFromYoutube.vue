<!--<template>-->
<!--  <div>-->
<!--      <form>-->
<!--        <div v-for="item in playListData">-->
<!--          <input :key="item.title" type="checkbox" :value="item.title" @click="addSongToPlaylist"> {{ item.title }} -<a :key="item.title" :href="`https://www.youtube.com/watch?v=${item.videoId}`" target="_blank">Przesłuchaj kawałek</a>-->
<!--        </div>-->
<!--        <button type="submit">-->
<!--          Dodaj do playlisty-->
<!--        </button>-->
<!--      </form>-->
<!--  </div>-->
<!--</template>-->

<!--<script setup lang="ts">-->
<!--import {onBeforeMount, ref,watchEffect} from 'vue'-->

<!--const ApiKey = "AIzaSyCNKSMO5i8RFdHYSIuuO0zVl0FCPPl5VfA"-->
<!--const playListId = "PLWfiGYuvhOCv11AUOF-CC_fY7Hktfq4Cl"-->
<!--const playListData = ref([])-->

<!--const fetchData = async () => {-->
<!--  const response = await fetch(`https://youtube.googleapis.com/youtube/v3/playlistItems?part=snippet&maxResults=150&playlistId=${playListId}&key=${ApiKey}`)-->
<!--  const data = await response.json()-->
<!--  data.items.forEach((item: any) => {-->
<!--    playListData.value.push({-->
<!--      title: item.snippet.title,-->
<!--      videoId: item.snippet.resourceId.videoId,-->
<!--    })-->
<!--  })-->
<!--}-->
<!--onBeforeMount(() => {-->
<!--  fetchData()-->
<!--})-->

<!--const playlist = ref([])-->

<!--const addSongToPlaylist = (event) => {-->
<!--  if (event.target.checked) {-->
<!--    playlist.value.push(event.target.value)-->
<!--  } else {-->
<!--    playlist.value = playlist.value.filter((item: any) => item !== event.target.value)-->
<!--  }-->
<!--}-->
<!--watchEffect(() => {-->
<!--  console.log(playlist.value)-->
<!--})-->




<!--</script>-->

<!--<style scoped>-->

<!--</style>-->
