<template>
    <div id="songList-container">
        <h1>Song Lists</h1>
        <div class="songs-list">
            <Song title="Title" artist="Artist" duration="3:08" />
        </div>
    </div>
</template>

<script>
import Song from './Song.vue'

export default {
    name: "SongList",
    components: {
        Song,
    }    
}
</script>

<style scoped>
    #songList-container{
        display: grid;
        background-color: lightblue;
        border: 1px solid black;
        width: 90%;
        height: 90%;
    }
    h1{
        text-align: center;
    }
</style>