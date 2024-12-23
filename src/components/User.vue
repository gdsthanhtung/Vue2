<template>
  <div class="user">
    <p>Comp user</p>
    <p>{{ user.name }}</p>
    <p>{{ user.email }}</p>
    <p>{{ user.age }}</p>
    <p>{{ user.active }}</p>
    <button class="delete" v-on:click="deleteUser(user)">Delete</button>
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
  },
  methods: {
    deleteUser(user) {
      console.log('delete user', user);
      this.$emit('deleteUser', user)
    }
  }
}
</script>

<style>
  .user {
    position: relative;
  }

  .user .delete {
    position: absolute;
    top: 0;
    right: 0;
    background-color: orange;
    color: white;
    border: none;
    padding: 5px 10px;
    cursor: pointer;
  }
</style>
