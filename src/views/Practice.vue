<template>
  <html>
    <div>
      <input type="number" v-model="inputNum" />
      &nbsp
      <button type="button" @click="multiFormula(inputNum)">
        按我算出階層
      </button>
      <br />
      {{ result }}
    </div>
  </html>
</template>

<script lang="ts" setup>
import { ref } from "vue";
let inputNum: number;
let result = ref(""); /* 呼叫multiFormula */

/* 課堂練習 */
function multiFormula(inputNum: number) {
  // /* 設定需要的變數 */
  // let i: ;
  // let factorial = 1;
  // let formula: ;
  // /* 回圈乘出最終答案 */
  // for (i = inputNum; i >= 1; i--) {
  //   factorial = factorial*;
  //   formula = ;
  // }
  // /* 組成算式 */
  // formula = ;

  // /* 回傳給result */
  // result.value = formula;
}
</script>
