<template>
    <ul>
        <!--p> {{ randomInsult }} </p>
        <button v-on:click="show">
            get insult
        </button>-->
        <input v-model="play" placeholder="Play">
        <input v-model="insult" placeholder="Insult">
        <button v-on:click="newItem"> Create new insult </button>

    </ul>
</template>

<script>
export default {
    data: () => {
        return {
            play: "play",
            insult: "insult",
            object: {}
        }
    }, properties: {

    },
    methods: {
        newItem: function() {
            this.$emit("addNewInsult", {play: this.play, insult: this.insult})
        },
    }
}
</script>

<style>

</style>