<template>
  <button @click="debouncedClick">save button</button>
</template>

<script>
import _ from 'lodash'

export default {
  name: "SaveButton",
  created() {
    this.debouncedClick = _.debounce(this.click, 2000)
  },
  unmounted() {
    this.debouncedClick.cancel()
  },
  methods: {
    click() {
      console.log("clicked!!")
    }
  }
}
</script>

<style scoped>

</style>