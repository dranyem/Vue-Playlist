<template>
  <div id="app">
    <SongList :songlist="listOfSongs"
              @addSongPlayList="addToPlaylist" />
    <PlayList :playSongList="listOfPlaySongs"
              @removeSongFromPlaylist="removeSong"/>
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
            listOfPlaySongs: [

            ],
        }
    },
    methods: {
      addToPlaylist: function(song){
        for(var i=0; i<this.listOfSongs.length; i++){
          if(song.title == this.listOfSongs[i].title){
            this.listOfPlaySongs.push(this.listOfSongs[i]);
            this.listOfSongs.splice(i,1);
            break;
          }
        }
      },
      removeSong(song){
        for(var i=0; i<this.listOfPlaySongs.length; i++){
          if(song.title == this.listOfPlaySongs[i].title){
            this.listOfSongs.push(this.listOfPlaySongs[i]);
            this.listOfPlaySongs.splice(i,1);
            break;
          }
        }
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
  place-items: center;
  width: 100%;
  height: 95vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
