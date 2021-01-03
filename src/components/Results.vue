<template>
  <p>Reaction time: {{score}} ms </p>
  <p class="ranks"> {{rank}} </p>
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
        if(this.score < 250) {
            this.rank = 'Fire fingers!'
        } else if (this.score < 400) {
            this.rank = 'Amazing!'
        } else {
            this.rank = 'A little slow...'
        }
    }
}
</script>

<style>
    .ranks {
        font-size: 1.4em;
        color: green;
        font-weight: bold;
    }

</style>