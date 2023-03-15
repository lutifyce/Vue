<script>
export default {
  data() {
     return {
      message: "Задание",
      message1: 1,
	}
  },
  methods: {
   
    },
  },
};
</script>
<template>
  <input type="text" v-model="message" />
<p>{{ message }}</p>
<p>{{ message.toUpperCase() }}</p>
<input type="number" v-model="message1" />
<p>{{ message1 ** 2 }}</p>
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