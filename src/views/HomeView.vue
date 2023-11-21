

<template>
  <main id="paopao-box">
    <div class="text-box" v-for="item in paopaoNameList"><div class="text">{{item}}</div></div>
  </main>
</template>


<script setup>
import { ref } from 'vue';
let paopaoNameList = ref(["知识","游戏","日常","笔记","POWER"])
</script>

<style scoped lang="scss">
#paopao-box{
  display: flex;
  transform: translate(50%,50%);
  left: -50%;
  top: -50%;
  justify-content: space-around;
    .text-box{
      border-radius: 25%;
      width: 88px;
      height: 88px;
      text-align: center;
      line-height: 88px;
      background: linear-gradient(45deg,blue 0%,pink 50%);
      margin: 0 27px 0 8px;
      animation: roll 5s linear infinite;
      box-shadow: 0 0 5px wheat;
      &:hover{
        cursor: pointer;
        animation: changeShape 1s forwards;
      }
      .text{
        animation: roll 5s linear infinite;
        animation-direction: reverse;
        &:hover{
          cursor: pointer;
          animation: changeShape 1s;
          animation-direction: reverse;
        }
      }
    }
}

@keyframes roll {
  0%{
    transform: rotateZ(0);
  }
  100%{
    transform: rotateZ(360deg);
  }
}
@keyframes changeShape {
  0%{
    transform: rotateZ(0);
    border-radius: 25%;
  }
  100%{
    transform: rotateZ(1080deg);
    border-radius: 50%;
  }
}


</style>