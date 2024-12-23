<template>
  <div class="comp-tab">
    <div class="tab-title">
      <span class="title">Tiêu đề của Tab</span>
      <i class="icon">icon</i>
    </div>

    <div class="tab-content">
      <slot name="tabList"></slot>
    </div>

    <div class="tab-content">
      <slot name="tabContent"></slot>
    </div>

  </div>
</template>

<script>
export default {
  name: 'CompTab',
  data() {
    return {

    }
  }
}
</script>
