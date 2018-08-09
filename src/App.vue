<template>
  <div id="app">
    <html>
      <body>
        <Header />
        <main> 
          <Profiles v-bind:dinosArray="dinos" />
        </main>
        <Footer /> 
      </body>
    </html>  
  </div>
</template>

<script>
import Header from './components/Header'
import Profiles from './components/Profiles'
import Footer from './components/Footer'


export default {
  name: 'App',
  components: {
    Header,
    Profiles,
    Footer
  },
  data() {
        return {
            dinos: [],
            apiURL: "../static/dinosaurs.json"
        }
  },
  created() {
    fetch(this.apiURL)
      .then(response => response.json())
      .then((json) => {
        return json;
      })
      .then(json => this.dinos = json)
  }
}
</script>

<style>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
html {
  margin: 0;
  padding: 0;
}
body {
  margin: 0 30px 0 30px;
  padding: 0;
  font-family: sans-serif;
  color: #1B997A;
  display: grid;
  grid-template-rows: 15% 75% 10%;
}
main {
  grid-row: 2/3;
}
main section {
  padding: 0 20px 0 20px;
  display: grid;
  grid-template-columns: repeat(auto-fit, x100%);
  grid-gap: 10px;
  margin: 0 auto;
  width: 50%;
}
small {
  color: black;
  font-size: .5rem;
  margin-left: 10px;
}
p {
  font-size: .8rem;
}

</style>
