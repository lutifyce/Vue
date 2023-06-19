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
  }
}
</script>

<template>
<User @show="userName"/>
</template>


<style scoped>
</style>