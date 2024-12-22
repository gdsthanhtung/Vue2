<template>
  <div>
    <p>{{ msg }}</p>
    <img src="../assets/logo.png">
    <p>{{ msgHeader }}</p>
    <button v-on:click="changeMsgEvent()">Click to change msgFooter through App.vue</button>
  </div>
</template>

<script>
export default {
  name: 'CompHeader',
  props: {
    msgHeader: String
  },
  methods: {
    changeMsgEvent() {
      let data = {
        msg: 'Change msgFooter from CompHeader.vue through event at app.vue!'
      }
      this.$emit('changeMsgEvent', data)
    }
  },
  data() {
    return {
      msg: 'Header'
    }
  }
}
</script>

<style scoped>
  h1 {
    color: red;
  }
</style>
