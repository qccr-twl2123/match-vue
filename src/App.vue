<template>
  <div id="app">
    <img src="./assets/logo.png">
    <button class="btn btn-primary">确定</button>
    <button class="btn btn-success">使用</button>
    <button class="btn btn-danger" @click="toNew">注意</button>
    <router-link to="/girl">girl</router-link>

    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    toNew () {
      window.open('./#/girl')
    }
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
