<template>
  <div class="slot">
    <slot name="header"></slot>
    <slot name="content"></slot>
    <CompTab title="Tiêu đề của tab-x">
      <ul slot="tabList" class="tab-header">
        <li class="tab-item" :class="{ 'tab-item-active' : tabActive ==  index}" v-for="(tab, index) in tabHeader" :key="tab.id" v-on:click="handleChangeTab(tab.id)">{{ tab.title }}</li>
      </ul>
      <div slot="tabContent" class="tab-content">
        <p>{{ tabHeader[tabActive].content }}</p>
      </div>
    </CompTab>
  </div>
</template>

<script>
import CompTab from './CompTab.vue'
export default {
  name: 'CompSlot',
  components: { CompTab },
  data() {
    return {
      tabHeader: [
        {id: 1, title: 'Tab 1', content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos, quae 1'},
        {id: 2, title: 'Tab 2', content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos, quae 2'},
        {id: 3, title: 'Tab 3', content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos, quae 3'},
        {id: 4, title: 'Tab 4', content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos, quae 4'},
        {id: 5, title: 'Tab 5', content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos, quae 5'},
      ],
      tabActive: 0
    }
  },
  methods: {
    handleChangeTab(id) {
      this.tabActive = id-1;
    },
  }
}
</script>

<style>
.slot {
  border: 1px solid #7700ff;
  padding: 20px;
  margin: 20px 0;
}
.tab-item {
  display: inline-block;
  padding: 10px 20px;
  border: 1px solid #7700ff;
  margin-right: 10px;
  cursor: pointer;
  justify-content: space-between;
}
.tab-item-active {
  background-color: #7700ff;
  color: white;
}
</style>
