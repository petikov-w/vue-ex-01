<template>
  <div id="app">
    <div class="wrapper">
      <div class="header">
        <img id="logo-header" src="./assets/image/logo.png" alt="">
        <MainMenu></MainMenu>
      </div>
      <div class="content">

      </div>
      <div class="footer">
        <img id="logo-footer" src="./assets/image/logo.png" alt="">
        <Copyright></Copyright>
      </div>
    </div>
  </div>
</template>

<script>
import MainMenu from './components/MainMenu.vue'
import Copyright from './components/Copyright.vue'

export default {
  name: 'App',
  components: {
    MainMenu,
    Copyright
  }
}
</script>

<style lang="scss">
@import "./assets/scss/variables";
  .wrapper {
    width: 70%;
    margin: auto;
  }
  .header {
    display: flex;
    justify-content: space-between;
    border-bottom: 2px solid $border-color;
  }
  .footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 2px solid $border-color;
    padding-top: 10px;
  }
  .content {
    min-height: 78vh;
  }

  #logo-header {
      height: 60px;
      width: 60px;
  }

  #logo-footer {
    height: 50px;
    width: 50px;
  }

</style>


