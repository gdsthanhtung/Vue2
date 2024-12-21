<template>
  <div>
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'CompFooter',
  data() {
    return {
      msg: 'Footer'
    }
  }
}
</script>

<style scoped>
  h1 {
    color: red;
  }
</style>
