<template>
  <div id="app" class="app">
    <Nav class="nav"></Nav>
    <div class="container">
      <Header class="header"></Header>
      <Cards class="cards"></Cards>
      <!-- <AreaChart /> -->
      <Chart />
      <Charts />
      <Table />
    </div>
  </div>
</template>

<script>
import Nav from './components/Nav.vue';
import Header from './components/Header.vue';
import Cards from './components/Cards.vue';
import Chart from './components/Chart.vue';
import Charts from './components/Charts.vue'
import Table from './components/Table.vue'

export default {
  name: "App",
  components: {
    Nav, Header, Cards, Chart, Charts, Table
  },
};
</script>

<style lang="scss">
/*Font*/
// @import './assets/styles/variables.scss';
@import url("https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400;700&display=swap");
body{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
*{
  margin: 0;
  padding: 0;
}
#app {
  font-family: "Lato", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0!important;
  padding: 0!important;
  box-sizing: border-box;
}


//VARIABLES
$primary-default: #336cfb;
$primary-dark: #1f58e7;
$primary-hover: #1f58e7;
$primary-light: #a9c1fd;
$primary-lightest: #ebf0ff;

$neutral-black: #25282b;
$neutral-grey-dark: #52575c;
$neutral-grey: #a0a4a8;
$neutral-grey-light: #cacccf;
$neutral-grey-lighter: #dbdde0;
$neutral-divider: #e8e8e8;
$neutral-bg: #f6f8fb;
$neutral-white: #ffffff;

$yellow-default: #fac032;
$yellow-dark: #efad0a;
$yellow-light: #fcdf98;

$green-default: #16d090;
$green-dark: #03b575;
$green-light: #34eeae;

$red-default: #ff6760;
$red-dark: #e74f48;
$red-light: #ff7e77;

//DEFAULT STYLES
h1 {
  font-weight: bold;
  font-size: 56px;
  line-height: 70px;
  letter-spacing: 0.4px;
  color: $neutral-black;
}
h2 {
  font-weight: bold;
  font-size: 40px;
  line-height: 46px;
  letter-spacing: 0.2px;
  color: $neutral-black;
}
h3 {
  font-size: 28px;
  line-height: 34px;
  letter-spacing: 0.2px;
  color: $neutral-black;
}
h4 {
  font-weight: bold;
  font-size: 26px;
  line-height: 34px;
  letter-spacing: 0.2px;
  color: $neutral-black;
}
h5 {
  font-weight: bold;
  font-size: 20px;
  line-height: 26px;
  letter-spacing: 0.2px;
  color: $neutral-black;
}
h6 {
  font-size: 18px;
  line-height: 24px;
  letter-spacing: 0.1px;
  color: $neutral-black;
}
a{
  text-decoration: none;
  color: initial;
  &:hover{
    text-decoration: none;
    color: initial;
  }
}
//MIXINS
@mixin subtitle1 {
  font-weight: bold;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.1px;
  color: $neutral-black;
}
@mixin subtitle2 {
  font-weight: bold;
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.1px;
  color: $neutral-black;
}
@mixin body1 {
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.1px;
  color: $neutral-black;
}
@mixin body2 {
  font-size: 14px;
  line-height: 20px;
  letter-spacing: 0.1px;
  color: $neutral-black;
}
@mixin small1 {
  font-size: 13px;
  line-height: 16px;
  letter-spacing: 0.1px;
  color: $neutral-black;
}
@mixin small2 {
  font-weight: bold;
  font-size: 12px;
  line-height: 16px;
  letter-spacing: 0.1px;
  color: $neutral-black;
}
@mixin small3 {
  font-weight: bold;
  font-size: 10px;
  line-height: 12px;
  letter-spacing: 0.2px;
  color: $neutral-black;
}
@mixin button {
  font-weight: bold;
  font-size: 14px;
  line-height: 18px;
  letter-spacing: 0.2px;
  color: $neutral-black;
}
@mixin initials {
  font-weight: 900;
  font-size: 13px;
  line-height: 16px;
  letter-spacing: 1px;
  color: $neutral-black;
}

//Shadow
@mixin shadow {
  box-shadow: 4px 0px 16px rgba(16, 30, 115, 0.08);
  background: $neutral-white;
}
@mixin right-divider {
  background: $neutral-white;
  border-right: $neutral-divider solid 1px;
}

.app{
  display: grid;
  grid-template-columns: 20% 80%;
  background: $neutral-bg;
}

// @media (max-width: 550px) {
//   .app{
//     grid-template-columns: 100%;
//   }
//   .nav{
//     display: none;
//   }
//}
</style>
