<template>
<div>
  <h2>News-content</h2>
  <p>NewsId: {{$route.params.id}}</p>
  <ul>
    <li><nuxt-link to="/">HOME</nuxt-link></li>
    <li><nuxt-link to="/news">News</nuxt-link></li>
  </ul>
</div>
</template>
<script>
export default {
  validate({params}) {
    return /^\d+$/.test(params.id)
  },
  asyncData(context) {
    // this.id = context;
    console.log(context)
    return {
      id: context.params.id
    }
  },
  data() {
    return {
      title: this.$route.params.title
    }
  },
  head() {
    return {
      title: this.title,
      meta: [
        {hid: 'description', name: 'news1', content: 'this is news page'}
      ]
    }
  }
}
</script>
<style scoped>
</style>
