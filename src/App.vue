<template>
  <div id="app">
    <el-container>
      <el-header>Header</el-header>
      <el-main><router-view/></el-main>
    </el-container>
  </div>
</template>

<script>
import
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
