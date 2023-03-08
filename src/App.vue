<script>
  export default {
    data() {
	return {
		name: 'luti',
		surn: 'fyce',
    text: 'page',
		href: 'page.html',
    num: 5,
    num1: 1,
		num2: 2,
		num3: 3,
    arr: ['x', 'y', 'z'],
    arr1: [1, 2, 3],
    obj: {x: 1, y: 2, z: 3},
    date : '4',
	}
},
methods: { 
 show: function() { 
  alert(today); 
 },
 summ: function() {
  alert(this.num1 + this.num2)
 },
 data: function(){
let date = this.dayOfWeek(this.date);
alert(date);
},
dayOfWeek: function(date){
let days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
return days[date-1];
},
}
}
  let today = new Date(); 
</script>


<template>
{{ summ() }}
  <div>
		<h1> App </h1>
	</div>
  <br>
  <div> <p> {{ name }} {{ surn }}</p>
  <p> paparam <a href="page.html">text</a></p>
  <p class="sc">num^2 = {{num*num}}, num1+num2+num3 = {{num1+num2+num3}}.</p>
  <p class="sc"> 1) <br> {{arr[0]}} <br> {{arr[1]}} <br> {{arr[2]}} <br> 2): {{arr1[0] + arr1[1] + arr1[2]}}</p><br>
  <p class="sc"> суммf элементов obj : {{obj.x + obj.y + obj.z}} </p>
  <button class="button button1" @click="show">Дата</button> <br> 
  <button class="button button2" @mouseenter="show"> Дата наводка</button> 
   <button class="button button1" @click="date">день недели({{ date }})</button>
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