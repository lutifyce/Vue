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
    asd() {
      alert('111');
    },
    aret(){
      alert('2222')
    }
  }
}
</script>

<template>
<User @show="asd" @show1="aret" />
</template>


<style scoped>
</style>