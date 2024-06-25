<template>
  <a-layout>
    <a-layout-header :style="headerStyle">Header</a-layout-header>
    <a-layout-content :style="contentStyle">
      <div>
        <component :is="currentComponent"></component>
        <button @click="switch_to_yi_yan">切换到一言</button>
        <button @click="switch_to_du_ji_tang">毒鸡汤</button>
        <button @click="switch_to_crazy_thursday">疯狂星期四</button>
      </div>
    </a-layout-content>
    <a-layout-footer :style="footerStyle">
      <Footer_diy></Footer_diy>
    </a-layout-footer>
  </a-layout>

</template>
<script>
import Show_random_data from "@/components/show_random_data.vue";
import Yi_yan_Component from "@/components/Yi_yan_Component.vue";
import Crazy_thursday from "@/components/crazy_thursday.vue";
import Footer_diy from '@/components/foo_diy.vue'
import {ref} from "vue";

const headerStyle = {
  textAlign: 'center',
  color: '#fff',
  height: 64,
  paddingInline: 50,
  lineHeight: '64px',
  backgroundColor: '#7dbcea',
};
const contentStyle = {
  textAlign: 'center',
  minHeight: 120,
  lineHeight: '120px',
  color: '#fff',
  backgroundColor: '#108ee9',
};
const footerStyle = {
  textAlign: 'center',
  color: '#fff',
  backgroundColor: '#7dbcea',
};
export default {
  name: 'App',
  components: {
    Yi_yan_Component,
    Show_random_data,
    Footer_diy,
    Crazy_thursday
  },
  setup() {
    const currentComponent = ref('Yi_yan_Component')

    function switch_to_yi_yan() {
      this.currentComponent = Yi_yan_Component
    }

    function switch_to_du_ji_tang() {
      this.currentComponent = Show_random_data
    }

    function switch_to_crazy_thursday() {
      this.currentComponent = Crazy_thursday
    }

    return {
      currentComponent,
      switch_to_yi_yan,
      switch_to_du_ji_tang,
      switch_to_crazy_thursday
    }
  },
  headerStyle,
  contentStyle,
  footerStyle
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
