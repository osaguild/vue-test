<template>
  <my-component v-model:title="bookTitle"></my-component>
  {{ bookTitle }}
</template>

<script>
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
</script>
