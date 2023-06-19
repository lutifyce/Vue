<script>
import User from './components/Employee.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    User
  },
  methods: {
    userName(name) {
      console.log(name);
    },
    userSalary(name, salary){
console.log(name, salary);
    }
  }
}
</script>

<template>
<User @show="userName" @show1="userSalary"/>
</template>


<style scoped>
</style>