<script>
export default {
  data() {
     return {
      choice: "",
      english: true,
      russian: false,
      python: false,
	}
  },
  methods: {
    eng: function () {
      this.english = true;
      this.russian = false;
      this.python = false;
    },
    rus: function () {
      this.english = false;
      this.russian = true;
      this.python = false;
    },
    py: function () {
      this.english = false;
      this.russian = false;
      this.python = true;
    },
  },
};
</script>
<template>
<p v-if="english">What is your mother tongue?</p>
  <p v-if="russian">Какой ваш родной язык?</p>
  <p v-if="python">
    print('hello world!') :)
  </p>
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="English"
    @click="eng"
  />
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="Русский"
    @click="rus"
  />
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="def def def"
    @click="py"
  />
  &nbsp;
  <p>{{ choice }}</p>
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