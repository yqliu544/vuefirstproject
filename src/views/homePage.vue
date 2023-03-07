<template>
<div>
  <header>
    <h1>
      大数据
    </h1>
  </header>
  <section class="container">
    <section class="itemleft"></section>
    <section class="itemcenter"></section>
    <section class="itemright"></section>
  </section>
</div>
</template>

<script>
export default {
  name: "homePage"
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
  border: 1px red;
  padding: .125rem .125rem 0;
  display: flex;
  .itemleft,.itemright{
    flex: 3;
  }
  .itemcenter{
    flex: 5;
  }
}
</style>
