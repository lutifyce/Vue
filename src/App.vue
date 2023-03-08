<script>
export default {
  data() {
    return {
       den:'ee',
       age:25,
    }
  },
  methods: {
     toggle: function() {
      this.isAdmin = !this.isAdmin;
    },
    denOfTheWeek: function() {
    this.den = new Date().getDay();
    },
  }
} 
</script>
<template>
  <button class="button" @click="toggle">{{ isAdmin ? "админ" : "не админ" }}</button><br>
  <p v-if="isAdmin">вы не админ</p>
  <p v-else>ладно вы админ..  </p>
  <br>
  <button class="button" @click="denOfTheWeek">тык</button><br>
  <p v-if="this.den === 1">Понедельник</p>
  <p v-if="this.den === 2">Вторник</p>
  <p v-if="this.den === 3">Среда</p>
  <p v-if="this.den === 4">Четверг</p>
  <p v-if="this.den === 5">Пятница</p>
  <p v-if="this.den === 6">Суббота</p>
  <p v-if="this.den === 0">Воскресенье</p>
  <br> <p class="button" v-if="age < 14">Вы ребенок</p>
  <p class="button"  v-else-if="age < 18">подросток</p>
  <p class="button"  v-else-if="age < 25">молодой человек</p>
  <p class="button"  v-else-if="age >= 26">мужчина</p>
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