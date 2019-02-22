<template>
  <div id="app">
    <Header/>
    <Home/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/header/HeaderComponent'
import Home from './components/home/HomeComponent'
import Footer from './components/footer/FooterComponent'

export default {
  name: 'app',
  components: {
    Header,
    Home,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
