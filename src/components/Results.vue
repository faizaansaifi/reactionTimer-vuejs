<template>
    <p>
    Reaction time- <span class="score"> {{ score }}ms</span>
  </p>
    <p class="rank"> {{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return{
            rank: null
        }
    },
    mounted() {
        if(this.score < 300){
            this.rank = 'Fastest Finger'
        }
        else if (this.score < 450) {
            this.rank = 'Rapid reflexes'
        }
        else {
            this.rank = '...Snail pace'
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
  .score {
    font-weight: bold;
  }
</style>