<template>
  <div>
    <h1>随机一句励志的话</h1>
    <h3 v-if="userName">{{ _type }}<b>     :     </b>{{ userName }} </h3>
    <button @click="randomizeUser">下一条</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import data from '../data/yi_yan_data.json'; // 假设 data.json 已经包含了用户数据

const userName = ref('');
const _type = ref("")
function randomizeUser() {
  const randomIndex = Math.floor(Math.random() * data.length);
  userName.value = data[randomIndex].text;
  _type.value = data[randomIndex].type;
}
</script>