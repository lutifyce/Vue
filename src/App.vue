<script>
  export default {
    data() {
	return {
		name: 'luti',
		surn: 'fyce',
    text: 'page',
		href: 'page.html',
    num: 5,
    num1: 4,
		num2: 3,
		num3: 2,
	}
}
  }
</script>

<template>
  <div>
		<h1> App </h1>
	</div>
  <br>
  <div> <p> {{ name }} {{ surn }}</p>
  <p> paparam <a href="page.html">text</a></p>
  <p class="sc">num^2 = {{num*num}}, num1+num2+num3 = {{num1+num2+num3}}.</p>
  </div>
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