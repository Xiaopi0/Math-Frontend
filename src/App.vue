<template>
  <div class="container" id="app">
    <Section Title="Math Frontend" Text="A Webpage for my solutions to Math Tasks" />
    <p>Input opgname. format: {type fx. FP9}_{dd}_{mm}_{yyyy}.json</p>
    <form v-on:submit="onSubmit(message)">
      <input class="theonlyfuckinginputonthepage" v-model="message">
    </form>
  </div>
</template>

<script>
import Section from './components/Section'

export default {
  name: 'App',
  components: {
    Section,
  },
  methods: {
    onSubmit(message) {
      
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
.theonlyfuckinginputonthepage {
  width: 5000;
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
