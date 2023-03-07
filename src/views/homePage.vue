<template>
<div>
  <header>
    <h1>
      大数据
    </h1>
  </header>
  <section class="container">
    <section class="itemleft">
      <ItemPage>
        <ItemOne/>
      </ItemPage>
      <ItemPage>
        <ItemTwo/>
      </ItemPage>
    </section>
    <section class="itemcenter"></section>
    <section class="itemright">
      <ItemPage>
        <ItemThree/>
      </ItemPage>
      <ItemPage>
        <ItemFour/>
      </ItemPage>
    </section>
  </section>
</div>
</template>

<script>
import ItemPage from "@/components/itemPage"
import ItemOne from "@/components/itemOne";
import ItemTwo from "@/components/itemTwo";
import ItemThree from "@/components/itemThree";
import ItemFour from "@/components/itemFour";
import {inject} from "vue";

export default {
  name: "homePage",
  components: {ItemPage,ItemOne,ItemThree,ItemTwo,ItemFour},
  setup(){
    let $echarts=inject("echarts")
    console.log($echarts)
  }
}
</script>

<style lang="less">
header{
  height: 1rem;
  width: 100%;
  h1{
    font-size: 0.375rem;
    text-align: center;
    line-height: 1rem;
  }

}
.container{
  min-width: 1200px;
  max-width: 2048px;
  margin: 0 auto;
  border: 1px solid red;
  padding: .125rem .125rem 0;
  display: flex;
  .itemleft,.itemright{
    flex: 3;
    border: 1px solid gold;

  }
  .itemcenter{
    flex: 5;
    border: 1px solid blue;
    margin: .25rem;
    padding: 0.125rem;

  }
}
</style>
