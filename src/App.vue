<script>
export default {
  data() {
     return {
     isDisabled: true,
	}
  },
  methods: {
    todayDate: function () {
      var today = new Date();
      this.dayYear = String(today.getDate());
      this.monthYear = String(today.getMonth() + 1);
      this.yearYear = today.getFullYear();
    },
  },
};
</script>
<template>
<input type="checkbox" :checked="isDisabled" @click="($event) => (this.isDisabled = !this.isDisabled)"/>
  <button class="button" v-bind:disabled="!isDisabled"
    @click="($event) => (this.isDisabled = !this.isDisabled)">
    {{ isDisabled ? "input включен" : "input выключен" }}
  </button>
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