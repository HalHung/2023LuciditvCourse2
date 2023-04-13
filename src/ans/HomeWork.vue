<template>
    <html>
      <div>
        <button type="button" @click="multiFormula()">按我印出九九乘法表</button>
        <br />
      </div>
    </html>
  </template>
  <script lang="ts" setup>
  /* 印出九九乘法表 */
  function multiFormula() {
    /* 設定需要的變數 */
    let i: number;
    let j: number;
    let formula: string = "";
    /* 回圈乘出最終答案 */
    for (i = 1; i <= 9; i++) {
      for (j = 1; j <= 9; j++) {
        formula = i + "*" + j + "=" + i * j;
        console.log(formula);
      }
      console.log("");
    }
  }
  </script>
  