<template>
<div>
  <h2>News</h2>
  <p>NewsId: {{$route.params.id}}</p>
  <p></p>
  <ul>
    <li><nuxt-link to="/">HOME</nuxt-link></li>
    <li><nuxt-link :to="{name: 'news-id', params: {id: 321, title:'i m title'}}">news-123</nuxt-link></li>
    <li><nuxt-link to="/news/hello">news-456</nuxt-link></li>

  </ul>
</div>
</template>
<script>
export default {
  transition: 'test',
  data() {
    return {
      id: ''
    }
  },
  // asyncData(context) {
  //   console.log(context.params)
  //   this.id = context.params.id;
  // },

}
</script>
<style scoped>
</style>
