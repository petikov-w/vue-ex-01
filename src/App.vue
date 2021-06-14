<template>
  <div id="app">
    <div class="wrapper">
      <LinkList></LinkList>
    </div>

  </div>
</template>

<script>
import LinkList from './components/LinkList.vue'

export default {
  name: 'App',
  components: {
    LinkList
  }
}
</script>

<style lang="scss">
    .wrapper {
      width: 80%;
      margin: auto;
    }
</style>


