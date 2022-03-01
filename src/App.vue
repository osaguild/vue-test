<template>
  <div>{{ count }}</div>
  <button @click="increment">Up vote</button>
</template>

<script>
export default {
  data() {
    return {
      count: 4
    }
  },
  methods: {
    increment() {
      this.count++
    }
  }
}
</script>