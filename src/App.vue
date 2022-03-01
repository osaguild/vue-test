<template>
  <div>
    <ol>
      <li v-for="(todo, index) in todos" :key="index">
        {{ todo.text }}
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [
        { text: 'learn javascript' },
        { text: 'learn vue' },
        { text: 'build something awesome' }
      ]
    }
  }
}
</script>