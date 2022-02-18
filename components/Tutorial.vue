<!-- Please remove this file from your project -->
<template>
  <div>
    <nuxt-link to="/">首页</nuxt-link>
    <nuxt-link to="/home">home</nuxt-link>
    <nuxt-link to="/about">about</nuxt-link>
    <nuxt-link to="/users">嵌套页面users</nuxt-link>

    <ul>
      <li v-for="item in list" :key="item.id">
        <nuxt-link :to="'/detail/' + item.id">{{item.name}}</nuxt-link>
      </li>

    </ul>
    <nuxt-child />
  </div>
</template>

<script>
export default {
  name: 'NuxtTutorial',

  data() {
    return {
      list: [
        {id: '01', name: 'aaa', price: '999'},
        {id: '02', name: 'bbb', price: '1000'},
        {id: '03', name: 'ccc', price: '2222'},
      ]
    }
  }
}
</script>
