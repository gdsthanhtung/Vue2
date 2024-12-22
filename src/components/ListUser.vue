<template>
  <div class="list-user">
    <p>Comp list user</p>
    <ul>
      <li v-for="user in listUser" :key="user.id">
        <User v-bind:user="user" />
      </li>
    </ul>
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
  }
}
</script>
