<template>
  <p>Reaction time: {{ score }}ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  name: "Results",  
  props: ['score'],
  data() {
      return {
          rank: null
      }
  },
  mounted() {
      if(this.score < 250) {
          this.rank = 'Ninja Speed'
      } else if (this.score < 400) {
          this.rank = 'Rapid Reflexes'
      } else {
          this.rank = 'Oops! Snail pace...'
      }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .rank {
      font-size: 1.4em;
      color: #0faf87;
      font-weight: bold;
  }
</style>
