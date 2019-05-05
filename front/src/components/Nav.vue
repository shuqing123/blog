<template>
  <div class="nav">
    <div class="wrap clearfix">
      <ul class="fl-l">
        <li class="fl-l active">首页</li>
        <li v-for="item in 3" class="fl-l">首页</li>
      </ul>
      <div class="search fl-l">
        <input type="text" placeholder="搜索问题或关键词">
      </div>
      <ul class="fl-r">
        <li class="fl-l login">立即登录</li>
        <li class="fl-l reg">免费注册</li>
      </ul>
    </div>
    <div id="main" style="width: 600px;height:400px;"></div>
  </div>
</template>

<script>
  export default {
    name: 'Nav',
    data() {
      return {

      }
    },
    mounted() {
    }
  }
</script>

<style scoped lang="less">
  .nav {
    background-color: @bg-c;
    border-bottom: 1px solid @bg-c - 20;
    padding: 10px 0;
    ul li {
      margin-right: 20px;
      padding: 0 20px;
      text-align: center;
      line-height: 30px;
      border-radius: 3px;
      cursor: pointer;
      &:hover {
        background-color: @bg-c - 30;
      }
      &.login {
        color: @theme;
      }
      &.reg {
        background-color: @theme;
        color: #fff;
        &:hover {
          background-color: @theme - 10;
        }
      }
    }
  }
  .active {
    color: @theme;
    font-weight: bold;
  }
  .search {
    border-radius: 3px;
    border: 1px solid @bg-c - 20;
    input {
      padding-left: 10px;
      width: 200px;
      border: none;
      outline: none;
      line-height: 26px;
    }
  }
</style>
