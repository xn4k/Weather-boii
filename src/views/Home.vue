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

const axios = require("axios");

let api_key = '31af009d0emsh31086eda8f02b30p131b82jsn7ea985ba33de';
const options = {
  method: 'GET',
  url: 'https://weatherbit-v1-mashape.p.rapidapi.com/forecast/3hourly',
  params: {lat: '35.5', lon: '-78.5'},
  headers: {
    'X-RapidAPI-Key': api_key,
    'X-RapidAPI-Host': 'weatherbit-v1-mashape.p.rapidapi.com'
  }
};

axios.request(options).then(function (response) {
  console.log(response.data);
}).catch(function (error) {
  console.error(error);
});
</script>
