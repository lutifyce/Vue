<script>
export default {
  data() {
     return {
      value: "",
      value_button: "",
      value_array: "",
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
<input type="num" v-model="num" />
   <valuearea v-model="value"></valuearea>
  &nbsp;
  <p>{{ value }}</p>
  &nbsp;
  <valuearea v-model="value_button"></valuearea>
  &nbsp;
  <button class="button" @click="split_value">Массив</button>
  &nbsp;
  <ul v-for="elem in value_array">
    <li :key="key">
      {{ elem }}
    </li>
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