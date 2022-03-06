<template>
  <user-name v-model:first-name="firstName" v-model:last-name="lastName"></user-name>
  <span>{{firstName}}.{{lastName}}</span>
</template>

<script>
import UserName from './components/UserName.vue'

export default {
  name: 'App',
  data() {
    return {
      firstName: 'aaa',
      lastName: 'bbb'
    }
  },
  components: {
    UserName
  }
}
</script>