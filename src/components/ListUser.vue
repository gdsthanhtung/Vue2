<template>
  <div class="list-user">
    <p>Comp list user</p>
    <User />
    <User />
    <User />
    <User />
  </div>
</template>

<script>
import User from './User.vue'
export default {
  components: { User },
  name: 'ListUser',
  data() {
    return {

    }
  }
}
</script>
