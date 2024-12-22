<template>
  <div id="app">
    <button v-on:click="changeMsg()">Change headder + footer msg!</button>

    <CompHeader v-bind:msgHeader="msgHeader" v-on:changeMsgEvent="handleChangeMsg" />

    <h1>{{ msg }}</h1>

    <ListUser v-bind:listUser="listUser" />

    <CompFooter v-bind:msgFooter="msgFooter" />
  </div>
</template>

<script>
import CompHeader from './components/CompHeader.vue'
import CompFooter from './components/CompFooter.vue'
import ListUser from './components/ListUser.vue'
export default {
  components: { CompHeader, CompFooter, ListUser },
  name: 'app',
  methods: {
    changeMsg () {
      this.msgHeader = 'Header msg changed!'
      this.msgFooter = 'Footer msg changed!'
    },
    handleChangeMsg (data) {
      this.msgFooter = data.msg;
    }
  },
  data () {
    return {
      msg: 'Main content',
      msgHeader: 'Data from app.vue file send to CompHeader.vue file',
      msgFooter: 'Data from app.vue file send to CompFooter.vue file',
      listUser: [
        {id: 1, name: 'User 1', age: 20, email: 'user1@gmail.com', active: true},
        {id: 2, name: 'User 2', age: 21, email: 'user2@gmail.com', active: false},
        {id: 3, name: 'User 3', age: 22, email: 'user3@gmail.com', active: true},
        {id: 4, name: 'User 4', age: 23, email: 'user4@gmail.com', active: false},
        {id: 5, name: 'User 5', age: 22, email: 'user5@gmail.com', active: true},
        {id: 6, name: 'User 6', age: 23, email: 'user6@gmail.com', active: false}
      ]
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

.container {
  margin: 0 auto;
  max-width: 1170px;
  padding: 0 15px;
  min-height: 3000px;
}
</style>
