<template>
  <div>
    <h4>{{title}}</h4>
    <button @click="$emit('enlargeText',0.1)">enlarge text</button>
  </div>
</template>

<script>
export default {
  name: "BlogPost",
  props: ['title'],
  emits: ['enlargeText']
}
</script>

<style scoped>

</style>