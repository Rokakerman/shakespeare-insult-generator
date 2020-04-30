<template>
    <section>
        <generateInsult v-on:addNewInsult="addNewInsult"></generateInsult>
        <ul v-for="shakeSpear in shakespear" :key="shakeSpear.insult">
            <li> {{ shakeSpear.insult }} </li>
         </ul>
    </section>
</template>

<script>
import generateInsult from './components/generateInsult.vue'

export default {
    components: {
        generateInsult,
    },
    data: () => {
        return {
            shakespear: [
                { play: 'Macbeth', insult: 'Were such things here as we do speak about? Or have we eaten on the insane root That takes the reason prisoner?'},
                { play: 'Richard III', insult: 'Never hung poison on a fouler toad'},
                { play: 'Julius Ceasar', insult: 'He thinks too much: such men are dangerous'},
                { play: 'The Merchant of Venice', insult: 'Thou calledst me a dog before thou hadst a cause. But since I am a dog, beware my fangs'},
                { play: 'The Two Noble Kinsmen', insult: 'Give me your hand...I can tell your fortune. You are a fool'},
                { play: 'The Tempest', insult: 'He smells like a fish, a very ancient and fish-like smell, a kind of not-of-the-newest poor-John. A strange fish!'},
                { play: 'Macbeth', insult: 'It is a tale Told by an idiot, full of sound and fury, Signifying nothing'},
                { play: 'Titus Andronicus', insult: 'Alas, poor heart, that kiss is comfortless As frozen water to a starved snake'},
                { play: 'Henry IV, Part 2', insult: 'He hath eaten me out of house and home; he hath put all substance into that fat belly of his'},
                { play: 'Romeo and Juliet', insult: 'Out, you green-sickness carrion! Out, you baggage! You tallow-face!'}
            ],
        }
    }, methods: {
        addNewInsult: function(obj) {
            this.shakespear.push(obj)
        }
    }
}
</script>

<style>

</style>