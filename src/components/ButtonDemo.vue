<template>
  <h2>示例1</h2>
  <div>
    <Button>基础按钮</Button>
    <Button theme="button">基础按钮</Button>
    <Button theme="link">链接按钮</Button>
    <Button theme="text">文本按钮</Button>
  </div>
  <h2>示例2</h2>
  <div>
    <Button size="big">大大大</Button>
    <Button>普普通</Button>
    <Button size="small">小小小</Button>
  </div>
  <h2>示例3</h2>
  <div>
    <Button size="big" theme="link">大大大</Button>
    <Button>普普通</Button>
    <Button size="small" theme="text">小小小</Button>
  </div>
  <h2>示例4</h2>
  <div>
    <dir>
      <Button level="main">主要按钮</Button>
      <Button>普通按钮</Button>
      <Button level="danger">危险按钮</Button>
    </dir>
    <dir>
      <Button theme="link" level="main">主要链接按钮</Button>
      <Button theme="link">普通链接按钮</Button>
      <Button theme="link" level="danger">危险链接按钮</Button>
    </dir>
    <dir>
      <Button theme="text" level="main">主要文字按钮</Button>
      <Button theme="text">普通文字按钮</Button>
      <Button theme="text" level="danger">危险文字按钮</Button>
    </dir>
</template>

<script>
import Button from '../lib/Button.vue'
export default {
  components: {
    Button
  }
}
</script>

<style lang="scss" scoped>
</style>
