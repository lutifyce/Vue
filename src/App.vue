<script>
export default {
  data() {
    return {
      users: [
			{
				id: 1,
				name: 'name1',
				salary: 100,
				age: 30,
			},
			{
				id: 2,
				name: 'name2',
				salary: 200,
				age: 40,
			},
			{
				id: 3,
				name: 'name3',
				salary: 300,
				age: 50,
			},
		],
    };
  },
  methods: {
    removeValue: function (id) {
      this.customers = this.customers.filter((customer) => {
        return customer.id !== id;
      });
    },
  },
};
</script>
<template>
  <table>
    <tr>
      <th>Id</th>
      <th>Name</th>
      <th>Salary</th>
      <th>Age</th>
      <th>Remove</th>
    </tr>
    <tr v-for="customer in customers">
      <td>{{ customer.id }}</td>
      <td>{{ customer.name }}</td>
      <td>{{ customer.value }}</td>
      <td>{{ customer.age }}</td>
      <td><button class="button" @click="removeValue(customer.id)">remove</button></td>
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