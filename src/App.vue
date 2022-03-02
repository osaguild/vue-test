<template>
  <div>
    <p>has published books</p>
    <div>{{ publishedBooksMessageCompute }}</div>
    <div>{{ publishedBooksMessageMethod() }}</div>
  </div>
  <div>
    <p>now date</p>
    <div>{{ dateNowCompute }}</div>
    <div>{{ dateNowMethod() }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      author: {
        name: "John Doe",
        books: [
          'Vue 2 - Advanced Guide',
          'Vue 3 - Basic Guide',
          'Vue 4 - The Mystery'
        ]
      }
    }
  },
  computed: {
    publishedBooksMessageCompute() {
      return this.author.books.length > 0 ? 'Yes' : 'No'
    },
    dateNowCompute() {
      return Date.now()
    }
  },
  methods: {
    publishedBooksMessageMethod() {
      return this.author.books.length > 0 ? 'Yes' : 'No'
    },
    dateNowMethod() {
      return Date.now()
    }
  }
}
</script>