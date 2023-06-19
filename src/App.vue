<script>
import User from './components/Employee.vue'
import UserForm from './components/UserForm.vue'

export default {
  data() {
    return {
      users: [
        {
          id: 1,
          name: 'Jujuba',
          surn: 'Capybara'
        },
        {
          id: 2,
          name: 'Emran',
          surn: 'Lox'
        },
        {
          id: 3,
          name: 'Vova',
          surn: 'Spit'
        },
      ],
    }
  },
  components: {
    User, UserForm
  },
  methods: {
    add(name, surn){
      let id = this.users.length + 1;
      this.users.push({
        id, name, surn
      });
    }
  }
}
</script>

<template>
<UserForm @add="add"/>
</template>


<style scoped>
</style>