<template>
  <!-- eslint-disable -->
  <div class="home">
    <img alt="Vue logo"
         src="../assets/logo.png" >
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'homeApp',
  components: {
    HelloWorld
  }
}


</script>
