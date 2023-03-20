<script>
export default {
  data() {
    return {
      arr: ["1", "2", "3", "4", "5"],
    };
  },
  methods: {
    removeValue: function (index) {
      this.arr.splice(index, 1);
    },
  },
};
</script>
<template>
  <ul>
    <li v-for="(item, index) in arr" :key="index">
      <button class="button" @click="removeValue(index)">{{ item }}</button>
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