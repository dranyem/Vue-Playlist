<template>
    <div class="song">
        <h3>{{title}}</h3>
        <p>Song Artist : {{artist}}</p>
        <i>Song Duration : {{duration}}</i>
        <br>
        <button @click="addSong">Add To PlayList</button>
    </div>
</template>

<script>
export default {
    name: "Song",
    props: {
        title: {
            type: String,
            required: true,
        },
        artist:{
            type: String,
            required: true,
        },
        duration:{
            type: String,
            require: true,
        },
    },
    methods:{
        addSong: function(){
            console.log(' add button is clicked');
            this.$emit("addSongToPlaylist",{title: this.title, artist: this.artist, duration: this.duration});
        },
    }
}
</script>

<style scoped>
    .song{
        display: inline-block;
        border: 1px solid black;
        padding: 10px;
        margin: 10px;
        box-shadow: 5px 5px grey;
    }
    button{
        margin: 20px;
    }
</style>