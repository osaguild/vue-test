<template>
  <button @click="click">{{ count }}</button>
</template>

<script>
import _ from 'lodash'

export default {
  data() {
    return {
      count: 1
    }
  },
  methods: {
    click: _.debounce (function() {
      this.count++
    }, 2000)
  }
}
</script>