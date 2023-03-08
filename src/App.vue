<script>
export default {
  data() {
    return {
      arr: ['a', 'b', 'c'],
    }
  },
  methods: {
  add: function() {
		  this.arr.push('b');
  },
    delFirst: function() {
      this.arr.shift();
  },
    delLast: function() {
      this.arr.pop();
  },
    delSecondToLast: function() {
      this.arr.splice(-2, 1);
  },
    sortArr: function() {
      this.arr.sort();
  },
    reverseOrder: function() {
      this.arr.reverse();
  }
    }
} 
</script>
<template>
  <button class="button" @click.once="add">1</button>
  <button class="button" @click.once="delFirst">2</button>
  <button class="button" @click.once="delLast">3</button>
  <button class="button" @click.once="delSecondToLast">4</button>
  <button class="button" @click.once="sortArr">5</button>
  <button class="button" @click.once="reverseOrder">6</button>
  <ul v-for="elem in arr">
    <li>{{ elem }}</li>
  </ul><br>
</template>

<style scoped>
header {
  line-height: 1.5;
}
.logo {
  display: block;
  margin: 0 auto 2rem;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }
  .logo {
    margin: 0 2rem 0 0;
  }
  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>