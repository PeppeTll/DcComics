<template>
  <div>
    <img :src="card.thumb" alt="">
    <h4>{{card.series}}</h4>
    <p>{{card.price}}</p>
  </div>
</template>

<script>
export default {
  name: 'CardComp',
  props: {
    card: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style lang="scss" scoped>
  
</style>