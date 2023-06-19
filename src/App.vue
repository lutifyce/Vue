<script>
import User from './components/Employee.vue'
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
    User
  },
  methods: {
    remove(id) {
      this.users = this.users.filter((user) => {
        return user.id !== id;
      })
    }
  }
}
</script>

<template>
<User v-for   ="user in users"
		:id     ="user.id"
		:name   ="user.name"
		:surn   ="user.surn"
		@remove ="remove"
		:key    ="user.id"/>
</template>


<style scoped>
</style>