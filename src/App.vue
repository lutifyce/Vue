<script>
export default {
  data() {
    return {
      items: [1, -2, 3, -4, 5],
    }
  },
  methods: {

    }
} 
</script>
<template>
   <div v-for="num in items">
    <p v-if="num >= 0">{{ num }}&nbsp;</p>
  </div>
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