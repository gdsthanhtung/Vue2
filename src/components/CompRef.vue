<template>
  <div class="">
    <h1>Comp Ref</h1>

    <button class="avatar" v-on:click="fileInputAvatar">Click to select Image</button>
    <input type="file" style="display: none" ref="fileInputAvatar" />
  </div>
</template>

<script>
export default {
  name: 'CompRef',
  data() {
    return {

    }
  },
  methods: {
    fileInputAvatar() {
      this.$refs.fileInputAvatar.click()
    }
  }
}
</script>

<style>
  .avatar {
    color: #fff;
    background-color: #007bff;
    padding: 15px 20px;
    cursor: pointer;
    border: 1px solid #fff;
    border-radius: 5px;
  }
  .avatar:hover {
    color: #007bff;
    background-color: #fff;
    border: 1px solid #007bff;
  }
</style>
