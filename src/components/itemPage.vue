<template>
<div class="item">
  <slot> </slot>

</div>
</template>

<script>
export default {
  name: "itemPage"
}
</script>

<style lang="less">
.item{
  height: 5.125rem;
  border: 1px solid blue;
  margin: .25rem;
  padding: 0.1rem;
  background-color: rgba(12,20,255,.25);
}

</style>
