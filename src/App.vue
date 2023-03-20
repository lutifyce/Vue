<script>
export default {
  data() {
    return {
      var_1: "Task 1",
      ctrlcheck: false,
      var_2: "ctrl+link pressed",
    };
  },
  methods: {
    lag: function () {
      this.var_1 = this.$refs.textField.value;
    },
    leg: function (event) {
      if (event.ctrlKey) {
        this.ctrlcheck = true;
      }
    },
    LKM: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "left";
      }
    },
    PKM: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "right";
      }
    },
    CKM: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "middle";
      }
    },
  },
};
</script>
<template>
 <input type="text" @keyup.enter="lag" ref="textField" />
  <br>
  <p>{{ var_1 }}</p>
  <br>
  <a
    href=""
    @click="leg"
    @click.left="LKM"
    @click.right="PKM"
    @click.middle="CKM"
    target="_blank"
    >ссылка</a
  >
  <br>
  <p v-if="ctrlcheck">{{ var_2 }}</p>
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