<script>
export default {
  data() {
     return {
      checked:true,
      
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
<input type="checkbox" v-model="checked" />
  &nbsp;
  <p v-if="checked">{{ checked }}</p>
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