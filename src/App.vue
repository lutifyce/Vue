<script>
import User from './components/User.vue'
export default {
  data() {
    return {
      name: 'asdd',
      salary: '54444',
      age: '35',
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