<template>
  <router-view></router-view>
</template>

<script lang="ts">
import { ref, provide } from 'vue'
export default {
  name: 'App',
  setup () {
    const clientWidth = document.documentElement.clientWidth
    const menuVisible = ref(clientWidth<=500?false:true)
    provide('menu', menuVisible)
  }
}
</script>
