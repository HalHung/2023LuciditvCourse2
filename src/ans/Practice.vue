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
    /* 設定需要的變數 */
    let i: number;
    let factorial = 1;
    let formula: string = "";
    /* 回圈乘出最終答案 */
    for (i = inputNum; i >= 1; i--) {
      factorial *= i;
      formula = formula + i + "*";
    }
    /* 組成算式 */
    formula = formula.substring(0, formula.length - 1) + " = " + factorial; //5*4*3*2*1=120
    formula = inputNum + "! = " + formula; //5! = 5*4*3*2*1 = 120
    // formula = inputNum + "! = " + factorial; //5! = 120
  
    /* 回傳給result */
    result.value = formula;
  }
  </script>
  