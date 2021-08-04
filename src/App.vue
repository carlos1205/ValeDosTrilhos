<template>
  <Fragment id="app">
    <Header />
    <Main />
    <Footer />
  </Fragment>
</template>

<script>
  import Main from './views/Main';
  import Footer from './components/Footer';
  import Header from './components/Header';
  import {Fragment} from 'vue-fragment';

  export default{
    components: {
      Main,
      Footer,
      Header,
      Fragment
    }
  }
</script>

<style>
  * {
    font-family: 'Open Sans', sans-serif;
    text-align:justify;
  } 
  p {
    font-size: 1.3rem;
  }
  
</style>