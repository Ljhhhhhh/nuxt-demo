<template>
<div>
  <p>name: {{result.name}}</p>
  <p>age: {{result.age}}</p>
  <p>sex: {{result.sex}}</p>
  <p>job: {{result.job}}</p>
</div>
</template>
<script>
import axios from 'axios'

export default {
  data(){
    return {
      name: 'asyncData'
    }
  },
  // asyncData({isDev, route, store, env, params, query, req, res, redirect, error}) {
  //   // 组件渲染前的动作，没有this
  //   return axios.get('https://api.myjson.com/bins/18pwag').then(res => {
  //     return {
  //       result: res.data
  //     }
  //   })
  // },
  async asyncData({isDev, route, store, env, params, query, req, res, redirect, error}) {
    let {data} = await axios.get('https://api.myjson.com/bins/18pwag')
    return {
      result: data
    }
  },
}
</script>
<style scoped>
</style>
