<script>
export default {
  data() {
    return {
      user1: '100',
      user2: '200',
      user3: '300',
    }
  },
  methods: {

    }
  }
} 
</script>
<template>
   <ul>
    <li v-for="value in data">{{ value }}</li>
  </ul>
  <ul>
    <li v-for="(value, key) in data">{{ key }} - {{ value }}</li>
  </ul>
  <ul>
    <li v-for="(value, key, index) in data">{{ key }} - {{ value }} - {{ index }}</li>
  </ul>
  <ul>
    <li v-for="(value, key, index) in data">{{ key }} - {{ value }} - {{ index + 1 }}</li>
  </ul>
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