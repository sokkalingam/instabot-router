<template>
  <div id="app" class="container">
    <div class="logo row">
        <img class="logo" src="./assets/instabot-logo.png">
        <img class="logo" src="./assets/instabot-title.png">
    </div>
    <HelloWorld msg="Instabot Router"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  text-align: center;
  background-color: white;
}

html {
  height: 100vh;
}

body {
  background-image: url('./assets/instabot-bg.jpg');
  height: 100vh;
}

.logo {
  height: 50px;
  margin-top: 5px;
  margin-bottom: 10px;
}
</style>
