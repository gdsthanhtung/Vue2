<template>
  <div class="user">
    <p>Comp user</p>
    <p>{{ user.name }}</p>
    <p>{{ user.email }}</p>
    <p>{{ user.age }}</p>
    <p>{{ user.active }}</p>
  </div>
</template>

<script>
export default {
  name: 'User',
  props: {
    user: {
      type: Object,
      default: () => {}
    }
  },
  data() {
    return {

    }
  }
}
</script>
