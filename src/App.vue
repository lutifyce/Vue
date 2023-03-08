<script>
export default {
  data() {
    return {
      visibility: false,
      visibility_p1: false,
      visibility_p2: false,
      visibility_p3: false,
    }
  },
  methods: {
     changeVisibilityToTrue: function() {
      this.visibility = true;
    },
    changeVisibilityToFalse: function() {
      this.visibility = false;
    },
     toggle_p1: function() {
        this.visibility_p1 = !this.visibility_p1;
      },
      toggle_p2: function() {
        this.visibility_p2 = !this.visibility_p2;
      },
      toggle_p3: function() {
        this.visibility_p3 = !this.visibility_p3;
      },
  }
} 
</script>
<template>
  <p v-if="!hidden">P1</p>
  <button class="button" v-if="!visibility" @click="changeVisibilityToTrue">Show text</button>
  <button class="button" v-else @click="changeVisibilityToFalse">Hide text</button><br>
   <button class="button" @click="toggle_p1">toggle</button><br>
  <p v-if="visibility_p1">text p1</p>
  <button class="button" @click="toggle_p2">toggle</button><br>
  <p v-if="visibility_p2">text p2</p>
  <button class="button" @click="toggle_p3">toggle</button><br>
  <p v-if="visibility_p3">text p3</p>
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