<template>
  <my-component :propA="1" :propB="b" :propC="c" :propF="success"></my-component>
</template>

<script>
import MyComponent from './components/MyComponent.vue'

export default {
  name: 'App',
  components: {
    MyComponent
  }
}
</script>
