<template>
  <save-button></save-button>
</template>

<script>
import SaveButton from './SaveButton.vue'

export default {
  data() {
    return {
      count: 1
    }
  },
  components: {
    SaveButton
  }
}
</script>