<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer'
import Main from './components/Main'


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer

  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Indie Flower',cursive;
  font-size: 20px;
  text-shadow: 3px 3px 3px #ababab;
  line-height: 2.5em;
  background-color: #DEF3FF;
  background-color: #D9AFD9;
  background-size: cover;
  background-position: center;
  background-image: linear-gradient(0deg, #d9afd9 0%, #DEF3FF 100%);
  /* note this below */
  background-attachment: fixed;
}

#app{
  display: flex;
  flex-direction: column;
  height: 100vh;
  padding: 0 2rem;
  justify-content: space-between;
  align-items: center;
}

</style>
