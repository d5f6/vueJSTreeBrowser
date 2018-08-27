<template>
  <div>
    <div class="node">
      <h1>{{node.name}}</h1>
    </div>
    <TreeBrowser
      v-for="child in node.children"
      :key="child.name"
      :node="child"
    />
  </div>
</template>

<script>
export default {
  name: 'TreeBrowser',
  props: {
    node: Object
  }
}
</script>

<style>

</style>
