<template>
  <div>
    <div class="topnav">
      <div class="logo"></div>
      <ul class="menu">
        <li>菜单一</li>
        <li>菜单二</li>
      </ul>
    </div>
    <div class="banner">
      <h1>lea-ui</h1>
      <h2>练习的UI框架</h2>
      <p class="actions">
        <a href="">GitHub</a>
        <a href="">开始</a>
      </p>
    </div>
  </div>
</template>
<script lang="ts">
export default {

}
</script>
<style lang="scss" scoped>
.topnav {
  background: pink;
  display: flex;
  padding: 16px;
  > .logo {
    max-width: 6em;
    margin-right: auto;
  }
  > .menu {
    display: flex;
    white-space: nowrap;
    flex-wrap: nowrap;
    > li {
      margin: 0 1em;
    }
  }
}
</style>
