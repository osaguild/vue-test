<template>
  <custom-input :model-value="searchText" @update:model-value="searchText = $event"></custom-input>
    {{searchText}}
</template>

<script>
import CustomInput from './components/CustomInput.vue'

export default {
  name: 'App',
  data() {
    return {
      searchText: ''
    }
  },
  components: {
    CustomInput
  }
}
</script>