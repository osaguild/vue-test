<template>
  <div id="dynamic-component-demo" class="demo">
    <button v-for="(tab,index) in tabs" :key="index" :class="['tag-button',{active: currentTab === tab}]" v-on:click="currentTab = tab">{{tab}}</button>
    <component v-bind:is="currentTabComponent" class="tab"></component>
  </div>
</template>

<script>
import TabHome from './components/HomeComponent.vue'
import TabPosts from './components/PostsComponent.vue'
import TabArchive from './components/ArchiveComponent.vue'

export default {
  name: 'App',
  data() {
    return {
      currentTab: 'Home',
      tabs: ['Home','Posts','Archive']
    }
  },
  computed: {
    currentTabComponent() {
      return 'tab-' + this.currentTab.toLowerCase()
    }
  },
  components: {
    TabHome,
    TabPosts,
    TabArchive
  }
}
</script>
<style>
.demo {
  font-family: sans-serif;
  border: 1px solid #eee;
  border-radius: 2px;
  padding: 20px 30px;
  margin-top: 1em;
  margin-bottom: 40px;
  user-select: none;
  overflow-x: auto;
}

.tab-button {
  padding: 6px 10px;
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
  border: 1px solid #ccc;
  cursor: pointer;
  background: #f0f0f0;
  margin-bottom: -1px;
  margin-right: -1px;
}
.tab-button:hover {
  background: #e0e0e0;
}
.tab-button.active {
  background: #e0e0e0;
}
.demo-tab {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>