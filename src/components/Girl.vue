<template>
  <div>
    <el-button @click="show = !show">Click Me</el-button>

    <div style="display: flex; margin-top: 20px; height: 100px;">
      <transition name="el-fade-in-linear">
        <div v-show="show" class="transition-box">.el-fade-in-linear</div>
      </transition>
      <transition name="el-fade-in">
        <div v-show="show" class="transition-box">.el-fade-in</div>
      </transition>
    </div>
  </div>

</template>

<script>
export default {
  name: 'Girl',
  data () {
    return {
      girls: [],
      show: true
    }
  },
  created () {
    this.axios.post("http://www.hao1024.cn/girl.json").then(body => {
      this.girls = body.data
      console.log(this.girls)
    })
  }

}
</script>

<style scoped>
  ul{
    list-style-type: none;
  }
  .transition-box {
    margin-bottom: 10px;
    width: 200px;
    height: 100px;
    border-radius: 4px;
    background-color: #409EFF;
    text-align: center;
    color: #fff;
    padding: 40px 20px;
    box-sizing: border-box;
    margin-right: 20px;
  }

</style>
