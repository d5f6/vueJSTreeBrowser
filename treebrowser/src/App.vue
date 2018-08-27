<template>
  <div id="app">
    <TreeBrowser
      :node="root"
    />
  </div>
</template>

<script>
import TreeBrowser from './components/TreeBrowser'

export default {
  name: 'App',
  data() {
    return {
      root: {
        name: '/',
        children: [
          {
            name: 'music',
            children: [
              {
                name: 'song.mp3'
              }
            ]
          },
          {
            name: 'workspace',
            children: [
              {
                name: 'source.js'
              }
            ]
          }
        ]
      }
    }
  },
  components: {
    TreeBrowser
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
