<script>
export default {
  data() {
    return {
      visibility: false,
    }
  },
  methods: {
     changeVisibilityToTrue: function() {
      this.visibility = true;
    },
    changeVisibilityToFalse: function() {
      this.visibility = false;
    }
  }
} 
</script>
<template>
  <p v-if="!hidden">P1</p>
  <button class="button" v-if="!visibility" @click="changeVisibilityToTrue">Show text</button>
  <button class="button" v-else @click="changeVisibilityToFalse">Hide text</button><br>
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