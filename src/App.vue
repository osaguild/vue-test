<template>
  <ul>
    <li v-for="(item, index) in items" :key="index">
      {{ parentMessage }} - {{ index }} - {{ item.message }}
    </li>
    <br>
    <li v-for="(value,index) in myObject" :key="index">
      {{ value }}
    </li>
    <br>
    <li v-for="(value,name) in myObject" :key="name">
      {{ name }}: {{ value }}
    </li>
    <br>
    <li v-for="(value,name,index) in myObject" :key="index">
      {{ index }}. {{ name }}: {{ value }}
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      parentMessage: 'parent',
      items: [
          { message: 'Foo'},
          { message: 'Bar'}
      ],
      myObject: {
        title: 'How to do lists in Vue',
        author: 'Jane Doe',
        publishedAt: '2016-04-10'
      }
    }
  }
}
</script>