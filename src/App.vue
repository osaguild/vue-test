<template>
  <div class="static" :class="{ active: isActive, 'text-danger': hasError }"></div>
  <div :class="classObject"></div>
</template>

<script>
export default {
  data() {
    return {
      isActive: true,
      hasError: true,
      classObject: {
        active: true,
        'text-danger': true
      }
    }
  }
}
</script>