<template>
  <div class="result">
    <p>your score {{ score }} ms</p>
    <p class="rank"> {{ rank }} </p>
  </div>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null,
        }
    },

    mounted() {
        if (this.score < 250) {
            this.rank = "wow, awesome score you have a fast finger."
        } else if (this.score < 400) {
            this.rank = "not bad, keep trying, my niger"
        } else {
            this.rank = "wtf man, you loose your reaction bitch."
        }
    }
}
</script>

<style>
.rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
}
</style>