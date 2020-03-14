<template>
    <div id="playList-container">
        <h1>Your Play List</h1>
        <div class="songs-playList">
            <PlaySong v-for="playSong in playSongList"
             :key="playSong"
             :title="playSong.title"
             :artist="playSong.artist"
             :duration="playSong.duration" />
        </div>
    </div>
</template>

<script>
import PlaySong from './PlaySong.vue'
export default {
    name: "PlayList",
    components: {
        PlaySong,
    },
    props: {
        playSongList: Array,
    }
}
</script>

<style scoped>
    #playList-container{
        display: grid;
        background-color: lightgreen;
        border: 1px solid black;
        width: 90%;
        height: 100%;
    }
    h1{
        text-align: center;
    }
</style>