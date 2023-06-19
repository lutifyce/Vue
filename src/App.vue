<script>
import User from './components/Employee.vue'
export default {
  data() {
    return {
      name: 'aaaa',
      salary: '33333',
      age: '12',
    }
  },
  components: {
    User
  }
}
</script>

<template>
<User :name="name" :salary="salary" :age="age"/>
</template>


<style scoped>
</style>