<template>
  <div class="container" id="app">
    <HeaderWithButton title="test" bText="Test2" bColor="magenta" onClickEvent="test" />
    <Section Title="Test Section" Text="Test Section Text" />
    <SectionWithOCButton Title="Test SectionWithO-CButton" Text="Test SectionWithO-CButton Text" BText="Open/Close Button" BColor="blue" OnClickEvent="OpenClose1" />
  </div>
</template>

<script>
import HeaderWithButton from './components/HeaderWithButton'
import Section from './components/Section'
import SectionWithOCButton from './components/SectionWithO-CButton'

export default {
  name: 'App',
  components: {
    HeaderWithButton,
    Section,
    SectionWithOCButton
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
