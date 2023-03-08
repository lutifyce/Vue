<script>
export default {
  data() {
    return {
      hrefs: [
			{href: '1.html', text: 'text1'},
			{href: '2.html', text: 'text2'},
			{href: '3.html', text: 'text3'},
		  ],
      products: [
			{
				name: 'product1',
				price: 100,
				quantity: 5
			},
			{
				name: 'product2',
				price: 200,
				quantity: 4
			},
			{
				name: 'product3',
				price: 300,
				quantity: 3
			},
		],
    }
  },
  methods: {

    }
  }
} 
</script>
<template>
  1)&nbsp;|&nbsp;
  <ul v-for="smh in hrefs">
    <li><a href="{{ smh.href }}">{{ smh.text }}</a></li>
  </ul><br>
  2)&nbsp;|&nbsp;
  <table v-for="sale in sales">
    <tr>
      <td>{{ sale.name }}</td>
      <td>{{ sale.price }}</td>
      <td>{{ sale.quantity }}</td>
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