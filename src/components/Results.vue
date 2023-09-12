<template>
  <div>
    <p class="results">Reaction Time: {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
  </div>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 400) {
      this.rank = "Monu Fingers";
    } else if (this.score < 500) {
      this.rank = "Rapid Reflex";
    } else {
      this.rank = "Ashiq Pace...(The slowest)";
    }
  },
};
</script>

<style>
.results {
  width: 300px;
  border-radius: 20px;
  background: lightpink;
  color: black;
  text-align: center;
  padding: 50px 0;
  margin: 40px auto;
}
.rank {
  font-size: 1.4em;
  color: #0faf87;
  font-weight: bold;
}
</style>
