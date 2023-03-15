<script>
export default {
  data() {
     return {
       num: 1,
      num_abz: "111",
      num_1: 0,
      num_2: 0,
      sum_num: "0",
      text_1: "gfg",
      text_2: "fgf",
      fullName: "",
      Name: "",
      Surname: "",
      Patronymic: "",
	}
  },
  methods: {
   square: function () {
      this.num_abz = this.num ** 2;
    },
    sum: function () {
      this.sum_num = this.num_1 + this.num_2;
    },
    swap: function () {
      const temp = this.text_1;
      this.text_1 = this.text_2;
      this.text_2 = temp;
    },
    split: function () {
      this.Surname = this.fullName.split(" ")[0];
      this.Name = this.fullName.split(" ")[1];
      this.Patronymic = this.fullName.split(" ")[2];
    },
  },
};
</script>
<template>
<input type="num" v-model="num" />
  <button @click="square">Квадрат num</button>
  &nbsp;
  <p>{{ num_square }}</p>
  &nbsp;
  <input type="num" v-model="numero_uno" />
  <input type="num" v-model="numero_dos" />
  <button @click="sum">Сумма</button>
  &nbsp;
  <p>{{ sum_num }}</p>
  &nbsp;
  <input type="text" v-model="text_uno" />
  <input type="text" v-model="text_dos" />
  <button @click="swap">Замена</button>
  &nbsp;
  <input type="text" v-model="fullName" />
  <button @click="split">Поделить ФИО</button>
  <p>Фамилия = {{ userSurname }}</p>
  <p>Имя = {{ userName }}</p>
  <p>Отчество = {{ userPatronymic }}</p>
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