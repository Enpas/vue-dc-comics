<template>
  <section>

    <div class="cards">

      <div class="box-imgs">
        <img :src="singleCard.thumb" :alt="singleCard.series">
      </div>
      <h3>{{singleCard.series}}</h3>
      
    </div>

  </section>
</template>

<script>
export default {
  name: 'Card',
  props: {
    singleCard: Object
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

.cards {
  flex-basis: calc(100% / 6);
  margin-right: 20px;
  margin-bottom: 40px;
  .box-imgs {
    height: 190px;
    overflow-y: hidden;
    margin-bottom: 20px;
  }
  h3 {
    max-width: 190px;
    font-size: 14px;
    font-weight: 400;
    text-transform: uppercase;
    color: #FFF;
  }
}
</style>