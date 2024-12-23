<template>
  <div class="list-user">
    <User v-for="user in listUser" :key="user.id"
      v-bind:user="user"
      v-on:deleteUser="deleteUser"
      class="user" />
  </div>
</template>

<script>
import User from './User.vue'
export default {
  components: { User },
  props: {
    listUser: {
      type: Array,
      default: () => []
    }
  },
  name: 'ListUser',
  data() {
    return {

    }
  },
  methods: {
    deleteUser(user) {
      console.log('delete user', user);
      this.$emit('deleteUser', user);
    }
  }
}
</script>

<style>
  .list-user {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
  }

  .list-user .user{
    padding: 30px;
    margin-bottom: 30px;
    border: 1px solid #09f;
    width: calc(30% - 20px);
  }
</style>
