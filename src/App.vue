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

  export default{
    components: {
      Main,
      Footer,
      Header
    }
  }
</script>

<style>
  * {
    font-family: 'Open Sans', sans-serif;
  } 
  p {
    font-size: 1.3rem;
  }
</style>