<template>
<div>
  <h2 v-if="error.statusCode === 404">404!没有找到你需要的页面</h2>
  <h2 v-else>500!服务器错误</h2>
</div>
</template>
<script>
export default {
  props: ['error']
}
</script>
<style scoped>
</style>
