<template>
  <div id="app">
    <CompHeader />

    <h1>{{ msg }}</h1>

    <listUser />

    <CompFooter />
  </div>
</template>

<script>
import CompHeader from './components/CompHeader.vue'
import CompFooter from './components/CompFooter.vue'
import ListUser from './components/ListUser.vue'
export default {
  components: { CompHeader, CompFooter, ListUser },
  name: 'app',
  data () {
    return {
      msg: 'Main content'
    }
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

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
