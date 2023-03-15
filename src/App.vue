<script>
export default {
  data() {
     return {
      lang: [],
	}
  },
  methods: {
   split_value: function () {
      this.value_array = this.value_button.split(" ");
    },
  },
};
</script>
<template>
<input type="checkbox" v-model="lang" value="c" />
  &nbsp;
  <p>C</p>
  &nbsp;
  <input type="checkbox" v-model="lang" value="python" />
  &nbsp;
  <p>Python</p>
  <input type="checkbox" v-model="lang" value="javascript" />
  &nbsp;
  <p>JavaScript</p>
  &nbsp;
  <ul v-for="elem in lang">
    <li>{{ elem }}</li>
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