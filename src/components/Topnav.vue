<template>
  <div class="topnav">
    <div class="logo" @click="menuHandle">LOGO</div>
    <ul class="menu">
      <li>菜单一</li>
      <li>菜单二</li>
    </ul>
  </div>
</template>

<script lang="ts">
import { inject, Ref} from 'vue'
export default {
  setup () {
    const menuVisible = inject<Ref<boolean>>('menu')
    console.log('Topnav中的 meneuVisible: ' + menuVisible.value)
    const menuHandle = () => {
      menuVisible.value = !menuVisible.value
    }
    return { menuHandle }
  }
}
</script>

<style lang="scss" scoped>
.topnav {
  background: pink;
  display: flex;
  padding: 16px;
  position: relative;
  z-index: 10;
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
