<template>
  <section class="container">
    <h2>New Index Page</h2>
    <div class="diss">
      <img src="~static/no-result.png">
    </div>
    <ul>
      <li><nuxt-link :to="{name: 'news', params: {id: 123}}">News</nuxt-link></li>
      <li><nuxt-link :to="{name: 'about'}">About</nuxt-link></li>
      <li><nuxt-link :to="{name: 'index'}">Home</nuxt-link></li>
      <li><nuxt-link :to="{name: 'asyncData'}">asyncData</nuxt-link></li>
    </ul>
    <div class="demo"><div class="c">hello JieHui.Lu</div></div>
  </section>
</template>

<script>

export default {
}
</script>

<style>
  .diss{
    width: 100px;
    height: 300px;
    background-image: url('~static/no-result.png');
  }
</style>

