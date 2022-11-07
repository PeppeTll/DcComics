<template>
  <div id="app">
    <!-- header -->
    <Header />
    <!-- main -->
    <Main />
    <Market />
    <!-- footer -->
    <Footer />
  </div>
</template>

<script>
  import Header from './components/HeaderComp'
  import Main from './components/MainComp'
  import Market from './components/MarketComp'
  import Footer from './components/FooterComp'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Market,
    Footer
  }
}
</script>

<style lang="scss">
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

li {
  list-style: none;
}

a {
  text-decoration: none;
  color: initial
}
</style>
