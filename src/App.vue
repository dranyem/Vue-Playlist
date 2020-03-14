<template>
  <div id="app">
    <SongList />
    <PlayList />
  </div>
</template>

<script>
import SongList from './components/SongList.vue'
import PlayList from './components/PlayList.vue'
export default {
  name: "App",
  components: {
    SongList,
    PlayList,
  }
};
</script>

<style>
#app {
  margin: 0;
  padding: 0;
  display:grid;
  grid-template-columns: 1fr 1fr;
  gap: 25px;
  width: 100%;
  height: 100vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
