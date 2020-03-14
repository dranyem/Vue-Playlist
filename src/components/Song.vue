<template>
    <div class="song">
        <h1>{{title}}</h1>
        <p>{{artist}}</p>
        <i>{{duration}}</i>
        <br>
        <button>Add To PlayList</button>
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
    }
}
</script>

<style scoped>
    .song{
        display: block;
        border: 1px solid black;
        padding: 20px;
        margin: 20px;
        box-shadow: 10px 10px grey;
    }
    button{
        margin: 20px;
    }
</style>