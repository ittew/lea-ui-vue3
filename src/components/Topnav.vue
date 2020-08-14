<template>
  <div class="topnav">
    <div class="logo">LOGO</div>
    <ul class="menu">
      <li>菜单一</li>
      <li>菜单二</li>
    </ul>
    <aside class="toggleAside"  @click="menuHandle"></aside>
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
  justify-content: center;
  align-items: center;
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
  .toggleAside{
    width: 24px;
    height: 24px;
    background: red;
    position: absolute;
    left: 16px;
    top: 50%;
    transform: translateY(-50%);
    display: none;
  }
  @media (max-width:500px) {
    .logo{ margin: 0 auto; }
    .menu{ display: none; }
    .toggleAside{display: inline-block; }
  }
}
</style>
