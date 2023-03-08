<script>
  export default {
    data() {
	return {
		name: 'luti',
		surn: 'fice',
    text: 'page',
		href: 'page.html',
	}
}
  }
</script>

<template>
  <div>
		<h1> App </h1>
	</div>
  <br>
  <br>
  <br>
  <br>
  <img :src="attr">
  <div> <p> Hello, i'm {{ name }} {{ surn }}</p>
    <p>Check out my skills <a href="page.html">here</a></p>
  </div>
</template>

<style >
header {
  line-height: 1.5;
}
p {
  line-height: 2.5;
  font-size: large;
  letter-spacing: 2px;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  color: rgb(255, 0, 0);
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