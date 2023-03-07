<template>
  <div>
    <h2>图标1</h2>
    <div class="chart" id="oneChart">

    </div>
  </div>
</template>

<script>
import {inject, onMounted, reactive} from "vue";

export default {
  name: "itemOne",
  setup(){
    let $echarts=inject("echarts");
    const data_static=[{"title":"电视","num":124},{"title":"冰箱","num":25},{"title":"洗衣机","num":412},{"title":"马桶","num":200}]
   let data= reactive({})
   let xdata= reactive([])
   let ydata= reactive([])

    function setData() {
      xdata=data_static.map(v=>v.title)
      ydata=data_static.map(v=>v.num)
    }

    onMounted(()=>{
      setData();
      let mychart=$echarts.init(document.getElementById("oneChart"))
      mychart.setOption({
        grid:{
          top:"3%",
          left:"5%",
          containLabel:true
        },
        xAxis:{
          type:"value",

        },
        yAxis:{
          type:"category",
          data:xdata
        },
        series:[
            {
              type:"bar",
              data:ydata,
              itemStyle:{
                normal:{
                  barBorderRadius:[0,20,20,0],
                  color: new $echarts.graphic.LinearGradient(0,0,1,0,[
                      {
                        offset:0,
                        color: "#005eaa"
                      },
                      {
                        offset:0.5,
                        color: "#0ff5aa"
                      },
                      {
                        offset:1,
                        color: "#0b52ba"
                      },
                      {
                        offset:0,
                        color: "#c852ba"
                      }]
                  )
                }
              }
            }
        ]
      })
    })
    return{
      data,xdata,ydata,setData
    }

  }
}
</script>

<style scoped>
.chart{
  height: 4.5rem;
}
h2{
  height: .6rem;
  color: red;
  line-height: 0.6rem;
  font-size: 0.3rem;
  text-align: center;
}
</style>
