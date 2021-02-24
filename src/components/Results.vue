<template>
  <p>Reaction time: {{ score }} ms</p>
  <h2>{{ rank }}</h2>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'Ninja Fingers!'
        } else if (this.score < 350) {
            this.rank = 'Fast enough!'
        } else if (this.score < 450) {
            this.rank = 'Good, but you can better!'
        } else if (this.score < 600) {
            this.rank = 'Slow. Try again!'
        } else if (this.score >= 600) {
            this.rank = 'Do you even move, bro?'
        }
    }
}
</script>

<style scoped>
 h2 {
     color: brown;
 }
</style>