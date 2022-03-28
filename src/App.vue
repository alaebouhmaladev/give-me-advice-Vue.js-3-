<template>
  <div class="root">
    <header-page title="Give Me Advice"></header-page>
    <form-page></form-page>
    <footer-page></footer-page>
  </div>
</template>

<script>

import HeaderPage from './components/HeaderPage.vue';
import FormPage from './components/FormPage.vue';
import FooterPage from './components/FooterPage.vue';
import Quotes from './data/quote.json';

export default {
  name: 'App',
  components: {
    HeaderPage,
    FormPage,
    FooterPage,
  },
  provide(){
    return{
      quotes  : this.Quotes,
      message : 'This message from Provide'
    };
  },
  data() {
    return {
      Quotes,
    }
  },
}
</script>

<style>
@import "./assets/css/style.css";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
