<template>
  <div>
    <h1>疯狂星期四</h1>
    <h3 v-if="userName">{{ _type }}<b> : </b>{{ userName }} </h3>
    <button @click="randomizeUser">下一条</button>
  </div>
</template>

<script setup>
import {ref} from 'vue';
import data from '../data/crazy_thursday.json';

const userName = ref('');
const _type = ref("")

function randomizeUser() {
  const randomIndex = Math.floor(Math.random() * data.length);
  userName.value = data[randomIndex].text;
  _type.value = data[randomIndex].type;
}
</script>