<template>
  <div>
    <h1>{{ msg }}</h1>
    <p class="">{{ msgFooter }}</p>
  </div>
</template>

<script>
export default {
  name: 'CompFooter',
  props: {
    msgFooter: {
      type: String,
      default: 'Footer props'
    }
  },
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
