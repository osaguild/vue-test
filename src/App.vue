<template>
  <ol>
    <todo-item v-for="item in groceryList" :todo="item" :key="item.id"></todo-item>
  </ol>
</template>

<script>
import TodoItem from './components/TodoItem.vue'

export default {
  name: 'App',
  data() {
    return {
      groceryList: [
        { id: 0, text: 'Vegetables' },
        { id: 1, text: 'Cheese' },
        { id: 2, text: 'Whatever else humans are supposed to eat' }
      ]
    }
  },
  components: {
    TodoItem
  }
}
</script>