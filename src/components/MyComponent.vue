<template>
  <div>prop A:{{propA}}</div>
  <div>prop B:{{propB}}</div>
  <div>prop C:{{propC}}</div>
  <div>prop D:{{propD}}</div>
  <div>prop E:{{propE}}</div>
  <div>prop F:{{propF}}</div>
  <div>prop G:{{propG}}</div>
</template>

<script>
export default {
  name: "MyComponent",
  props: {
    propA: Number,
    propB: [Number, String],
    propC: {
      type: String,
      required: true
    },
    propD: {
      type: Number,
      default: 100
    },
    propE: {
      type: Object,
      default() {
        return { message: 'hello'}
      }
    },
    propF: {
      validator(value) {
        return ['success','warning','danger'].includes(value)
      }
    },
    propG: {
      type: Function,
      dafault() {
        return 'Default function'
      }
    }
  }
}
</script>