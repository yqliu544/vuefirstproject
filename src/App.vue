<template>
  <router-view/>
</template>
<script>
import * as echarts from "echarts";
import axios from "axios";
import {provide} from "vue";
export default {
  setup(){
    provide("echarts",echarts);
    provide("axios",axios);
  }
}
</script>
<style lang="less">
*{
  margin: 0px;
  padding: 0px;
}
</style>
