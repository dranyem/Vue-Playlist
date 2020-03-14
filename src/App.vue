<template>
  <div id="app">
    <SongList :songlist="listOfSongs" />
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
  },
  data: function(){
        return {
            listOfSongs: [
                {
                    title: "Dance Monkey",
                    artist: "Tones and I",
                    duration: "3:26",
                },
                {
                    title: "Blinding Lights",
                    artist: "The Weeknd",
                    duration: "4:01",
                },
                {
                    title: "Sweet Night",
                    artist: "V",
                    duration: "3:37",
                },
                {
                    title: "Stupid Love",
                    artist: "Lady Gaga",
                    duration: "2:57",
                },
                {
                    title: "Don't Start Now",
                    artist: "Dua Lipa",
                    duration: "3:51",
                },
                {
                    title: "One Margarita",
                    artist: "Luke Bryan",
                    duration: "4:12",
                },
                {
                    title: "Before You Go",
                    artist: "Lewis Capaldi",
                    duration: "3:44",
                },
                {
                    title: "Intentions (feat. Quavo)",
                    artist: "Justin Bieber",
                    duration: "3:15",
                },
                {
                    title: "Memories",
                    artist: "Maroon 5",
                    duration: "3:55",
                },
                {
                    title: "Circles",
                    artist: "Post Malone",
                    duration: "3:51",
                },
            ],
        }
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
  height: 95vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
