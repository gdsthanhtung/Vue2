<template>
  <div>
    <p>{{ msg }}</p>
    <img src="../assets/logo.png">
  </div>
</template>

<script>
export default {
  name: 'CompHeader',
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
