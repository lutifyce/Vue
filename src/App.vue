<script>
export default {
  data() {
    return {
      obj: {
        hidden: true,
      },
    };
  },
  methods: {
    setDone: function () {
      this.obj.hidden = !this.obj.hidden;
    },
  },
};
</script>
<template>
  <button class="button" @click="this.obj.hidden = false">2</button>
  <button class="button" @click="this.obj.hidden = true">3</button>
  <button class="button" @click="setDone">{{ obj.hidden ? "show" : "hide" }} 4</button><br />
  <p :class="obj">asdasd</p>
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
p.hidden {
	display: none;
}
</style>