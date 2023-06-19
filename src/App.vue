<script>
import User from './components/Employee.vue'
export default {
  data() {
    return {
      users: [
        {
          id: 1,
          name: 'asd',
          salary: 5343,
          age:21
        },
        {
          id: 2,
          name: 'aaaa',
          salary: 2320,
          age: 13
        },
        {
          id: 3,
          name: 'bbbb',
          salary: 12312123,
          age: 81
        },
      ],
    }
  },
  components: {
    User
  }
}
</script>

<template>
<User v-for="user in users" :name="user.name" :salary="user.salary" :age="user.age" :key="user.id" />
</template>


<style scoped>
</style>