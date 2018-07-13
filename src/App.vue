<template>
  <div id="app">
    <headNav></headNav>
    <router-view/>
  </div>
</template>

<script>
import headNav from '@/components/common/headNav'
export default {
  name: 'App',
  components:{
    headNav
  }
}
</script>

<style>
@import "../static/css/global.css";
@import "../static/css/letGlobal.less";
</style>
