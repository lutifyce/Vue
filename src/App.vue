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
    change(id, name, surn){
      this.users = this.users.map((user) => {
        if(user.id === id){
          user.name = name;
          user.surn = surn;
        }
        return user;
      });
    }
  }
}
</script>

<template>
<User v-for   ="user in users"
		:id     ="user.id"
		:name   ="user.name"
		:surn   ="user.surn"
		:key    ="user.id"
    @change="change"/>
</template>


<style scoped>
</style>