<script>
export default {
  data() {
    return {
      isAdmin: true,
    }
  },
  methods: {
     toggle: function() {
      this.isAdmin = !this.isAdmin;
    }
  }
} 
</script>
<template>
  <button class="button" @click="toggle">{{ isAdmin ? "админ" : "не админ" }}</button><br>
  <p v-if="isAdmin">вы не админ</p>
  <p v-else>ладно вы админ..</p>
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