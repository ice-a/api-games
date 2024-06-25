<script setup>
import {ref} from 'vue';

const top = ref(10);
</script>

<template>
  <a-affix :offset-top="top">
    <a-space>
      <a-button type="primary" @click="top += 10"><a href="http://qd.lideshan.top/my/" target="_blank">自动化签到</a>
      </a-button>
      <a-button type="primary" @click="top += 10"><a href="http://pan.lideshan.top/" target="_blank">木子的秘密</a>
      </a-button>
          <a-button type="primary" @click="top += 10"><a href="https://cook.lideshan.top/"
                                                   target="_blank">一位大厨的崛起之路</a></a-button>
      <a-button type="primary" @click="top += 10"><a href="https://tools.lideshan.top/" target="_blank">木子的工具箱</a>
    </a-button>
      <a-button type="primary" @click="top += 10"><a href="https://eat.lideshan.top/"
                                                   target="_blank">不知道吃什么就去看看</a></a-button>
      <a-button type="primary" @click="top += 10"><a href="https://remake.lideshan.top/public/index.html" target="_blank">重生之我在人间两万年</a>
    </a-button>
       <a-button type="primary" @click="top += 10"><a href="https://ip.lideshan.top/"
                                                   target="_blank">木子的ip信息,爆破他</a></a-button>
      <a-button type="primary" @click="top += 10"><a href="https://lideshan.top/" target="_blank">去访问有趣的木子</a>
    </a-button>
    </a-space>
  </a-affix>
</template>

<style scoped>

</style>