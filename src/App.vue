<template>
  <button @click="counter += 1">add 1</button>
  <p>the button above has been clicked {{counter}} times.</p>
  <button @click="greet">Greet</button>
  <button @click="say('hi')">say hi</button>
  <button @click="say('what')">say what</button>
  <button @click="warn('form cannot be submitted yet.',$event)">submit</button>
  <button @click="one($event), two($event)">one two</button>
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
      name: 'Vue.js'
    }
  },
  methods: {
    greet(event) {
      alert('hello ' + this.name + '!')
      if (event) {
        alert(event.target.tagName)
      }
    },
    say(message) {
      alert(message)
    },
    warn(message,event) {
      if(event){
        event.preventDefault()
      }
      alert(message)
    },
    one(event){
      alert('one:' + event.target.tagName)
    },
    two(event){
      alert('two:' + event.target.tagName)
    }
  }
}
</script>