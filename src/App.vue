<template>
  <div>
    <div>set full name:{{ this.fullName = 'first last' }}</div>
    <div>get first name: {{ firstName }}</div>
    <div>get last name: {{ lastName }}</div>
    <div>get full name: {{ fullName }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: '',
      lastName: ''
    }
  },
  computed: {
    fullName: {
      get() {
        return this.firstName + ' ' + this.lastName
      },
      set(newValue) {
        const names = newValue.split(' ')
        this.firstName = names[0]
        this.lastName = names[names.length - 1]
      }
    }
  }
}
</script>