<script>
export default {
  data() {
    return {
      items: [1, 2, 3],
    }
  },
  methods: {

    }
  }
} 
</script>
<template>
  <template v-for="obj in items">
	<p>&nbsp;{{ obj }}&nbsp;</p>
	<hr>
  </template>
  <ul v-for="obj in items">
      <li>
        <p>&nbsp;{{ obj }}&nbsp;</p>
      </li>
   <hr>
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