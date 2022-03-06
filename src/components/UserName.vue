<template>
  <input type="text" :value="firstName" @input="$emit('update:firstName',$event.target.value)">
  <input type="text" :value="lastName" @input="$emit('update:lastName',$event.target.value)">
</template>

<script>
export default {
  name: "UserName",
  props: ['firstName','lastName'],
  emits: ['update:firstName','update:lastName']
}
</script>