
<template>
  <div class="weather">
    <h1>hallloooooiiiiiiiii</h1>
    <p>Lets try to make an API call</p>
    <button class="apibutton">TESTBUTTON 4 the API</button>
    <p></p>



  </div>
</template>

<script>
export default {
  name: "Weather"
}

const axios = require('axios');

async function makeRequest() {

  const config = {
    method: 'get',
    url: 'https://api.weatherapi.com/v1/current.json?key=ffc4143944e6422ab0602017221806&q=Cologne'
  }

  let res = await axios(config)

  console.log(res);
}

makeRequest();
</script>

<style scoped>

</style>