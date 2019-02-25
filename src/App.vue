<template>
  <div id="app" style="width:300px;margin:0 auto;">
    <slide-verify @success="onSuccess" @fail="onFail" @refresh="onRefresh" text="向右滑动验证"></slide-verify>
    <div>{{msg}}</div>
  </div>
</template>

<script>
export default {
  name: "AppDemo",
  data() {
    return {
      msg: ""
    };
  },
  methods: {
    onSuccess() {
      this.msg = "verify success";
    },
    onFail() {
      this.msg = "";
    },
    onRefresh() {
      this.msg = "";
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
