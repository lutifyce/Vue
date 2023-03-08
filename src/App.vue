<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5],
    }
  },
  methods: {
      toggle: function() {
      this.visibility = !this.visibility;
    }
  }
} 
</script>
<template>
  <div class="red-box"><div v-for="elem in items">{{ elem }} &nbsp;</div></div> <br>
  <div class="red-box"><br><div v-for="elem in items">{{ elem ** 2 }} &nbsp;</div></div> <br> <br>
  <div class="red-box right"><div v-for="elem in items"><ul><li>{{ elem }}</li></ul>&nbsp;</div></div>
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