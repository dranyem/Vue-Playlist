<template>
    <div id="songList-container">
        <h1>Song Lists</h1>
        <div class="songs-list">
            <Song v-for="song in songlist"
             :key="song"
             :title="song.title"
             :artist="song.artist"
             :duration="song.duration" />
        </div>
    </div>
</template>

<script>
import Song from './Song.vue'

export default {
    name: "SongList",
    props:{
        songlist: Array,
    },
    components: {
        Song,
    },
    
}
</script>

<style scoped>
    #songList-container{
        display: grid;
        background-color: lightblue;
        border: 1px solid black;
        width: 90%;
        height: 100%;
    }
    h1{
        text-align: center;
    }
</style>