<template>
  <router-view></router-view>
</template>

<script lang="ts">
import { ref, provide } from 'vue'
import { router } from "./router";
export default {
  name: 'App',
  setup () {
    const clientWidth = document.documentElement.clientWidth
    const menuVisible = ref(clientWidth<=500?false:true)
    provide('menu', menuVisible)
    router.afterEach(() => {
      if (clientWidth <= 500) {
        menuVisible.value = false;
      }
    })
  }
}
</script>
