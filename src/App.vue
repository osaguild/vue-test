<template>
  <user-name v-model:first-Name="firstName" v-model:last-Name="lastName"></user-name>
  <span>{{firstName}}.{{lastName}}</span>
  <!--
  <my-component v-model:title="bookTitle"></my-component>
  {{ bookTitle }}
  -->
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
/*
import MyComponent from './components/MyComponent.vue'

export default {
  name: 'App',
  data() {
    return {
      bookTitle: 'aaa'
    }
  },
  components: {
    MyComponent
  }
}
 */
</script>