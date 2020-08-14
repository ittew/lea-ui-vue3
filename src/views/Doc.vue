<template>
  <div class="layout">
    <Topnav />
    <div class="content">
      <aside v-if="menuVisible">
        <h2>组件列表</h2>
        <ol>
          <li>
            <router-link to="/doc/switch">Switch 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/button">button 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/dialog">dialog 组件</router-link>
          </li>
          <li>
            <router-link to="/doc/tabs">dialog 组件</router-link>
          </li>
        </ol>
      </aside>
      <main>
        <router-view />
      </main>
    </div>
  </div>
</template>
<script lang="ts">
import Topnav from '../components/Topnav.vue'
import { Ref, inject } from 'vue';
export default {
  components: {
    Topnav
  },
  setup () {
    const menuVisible = inject<Ref<boolean>>('menu')
    console.log('Doc中的 meneuVisible: ' + menuVisible.value)
    return { menuVisible }
  }
}
</script>
<style lang="scss" scoped>
.layout {
  display: flex;
  flex-direction: column;
  height: 100vh;
  > .nav {
    flex-shrink: 0;
  }
  > .content {
    flex-grow: 1;
    padding-top: 60px;
    padding-left: 156px;
    @media (max-width: 500px) {
      padding-left: 0;
    }
  }
}
.content {
  display: flex;
  > aside {
    flex-shrink: 0;
  }
  > main {
    flex-grow: 1;
    padding: 16px;
    background: lightgreen;
  }
}
aside {
  background: lightblue;
  width: 150px;
  padding: 16px;
  position: fixed;
  top: 0;
  left: 0;
  padding-top: 70px;
  height: 100%;
  > h2 {
    margin-bottom: 4px;
  }
  > ol {
    > li {
      padding: 4px 0;
    }
  }
}
</style>

