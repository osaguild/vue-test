<template>
  <TodoItem msg="todo message"/>
</template>

<script>
import TodoItem from './components/TodoItem.vue'

export default {
  name: 'App',
  components: {
    TodoItem
  }
}
</script>