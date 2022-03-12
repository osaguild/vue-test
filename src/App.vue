<template>
  <div id="counter">
    {{ users[0].id }}, {{ users[0].name }}
    {{ users[1].id }}, {{ users[1].name }}
  </div>
</template>

<script>
import Users from "./data/users"
export default {
  data() {
    return {
      users: Users
    }
  }
}
</script>