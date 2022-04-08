<template>
  <div id="app">
    <Menu/>
    <Landing/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Menu from "./components/Menu.vue";
import Landing from "./components/Landing.vue";

@Component({
  components: {
    Menu,
    Landing
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import "./assets/scss/_colors.scss";

body {
  background-color: $background;
  margin: 0;
  padding: 0;
  font-size: 16px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $text-primary;
}

a {
  color: inherit;
}

#app {
  width: 100%;
  min-height: 100vh;  
}
</style>
