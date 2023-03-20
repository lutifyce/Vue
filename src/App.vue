<script>
export default {
  data() {
    return {
      developers: [
        {
          id: 1,
          name: "name1",
          salary: 100,
          age: 20,
          isEdit: false,
        },
        {
          id: 2,
          name: "name2",
          salary: 200,
          age: 21,
          isEdit: false,
        },
        {
          id: 3,
          name: "name3",
          salary: 300,
          age: 22,
          isEdit: false,
        },
      ],
    };
  },
  methods: {
    removeItem: function (id) {
      this.developers = this.developers.filter((developer) => {
        return developer.id !== id;
      });
    },
    edit: function (developer) {
      developer.isEdit = true;
    },
    save: function (developer) {
      developer.isEdit = false;
    },
  },
};
</script>
<template>
  <table>
    <tr>
      <th>ID</th>
      <th>Имя</th>
      <th>Зарплата</th>
      <th>Возраст</th>
    </tr>
    <tr v-for="developer in developers">
      <template v-if="!developer.isEdit">
        <td>{{ developer.id }}</td>
        <td>{{ developer.name }}</td>
        <td>{{ developer.salary }}</td>
        <td>{{ developer.age }}</td>
        <td><button @click="removeItem(developer.id)">remove</button></td>
        <td><button @click="edit(developer)">edit</button></td>
      </template>
      <template v-else>
        <td><input v-model="developer.id" /></td>
        <td><input v-model="developer.name" /></td>
        <td><input v-model="developer.salary" /></td>
        <td><input v-model="developer.age" /></td>
        <td><button @click="save(developer)">save</button></td>
      </template>
    </tr>
  </table>
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