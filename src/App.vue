<template>
  <div class="container" id="app">
    <button :onClick="getOpg">Click</button>
  </div>
</template>

<script>
import Section from './components/Section'

export default {
  name: 'App',
  methods: {
    getOpg() {
      const axios = require('axios');

      // Make a request for a user with a given ID
      axios.get('https://3003-turquoise-mammal-mphszaam.ws-eu04.gitpod.io/opg/FP9_03_12_2019.json')
        .then(function (response) {
          // handle success
          console.log(response);
          console.log(response.data);
        })
        .catch(function (error) {
          // handle error
          console.log(error);
        })
        .then(function () {
          // always executed
        });
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
  background: #000080;
}
.container {
  max-width: 5000px;
  margin: 30px auto;
  margin-left: 30px;
  margin-right: 30px;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
</style>
