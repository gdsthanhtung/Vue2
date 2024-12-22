<template>
  <div>
    <p>{{ msg }}</p>
    <img src="../assets/logo.png">
    <p>{{ msgHeader }}</p>
  </div>
</template>

<script>
export default {
  name: 'CompHeader',
  props: {
    msgHeader: String
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
