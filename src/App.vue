<template>
  <user-name v-model:first-Name="firstName" v-model:last-Name="lastName"></user-name>
  <span>{{firstName}}.{{lastName}}</span>
</template>

<script>
import UserName from './components/UserName.vue'

export default {
  name: 'App',
  data() {
    return {
      firstName: '',
      lastName: ''
    }
  },
  components: {
    UserName
  }
}
</script>
