<template>
  <main>

    <div class="container">
     <a href="#" class="current-series">Current series</a>
      <div class="box-card">
        <Card 
          v-for="(comic, index) in comics" :key="index"
          :singleCard="comic"
        />
      </div>
      <a href="#" class="load-more">load more</a>
    </div>

  </main>
</template>

<script>
import Card from '@/components/Card.vue'
import comics from '@/assets/data/dc-comics.js'

export default {
  name: 'Main',
   data() {
    return {
      comics
    }
  },
  components: {
    Card
  }
}
</script>

<style lang="scss" scoped>
  @import '../assets/style/vars.scss';
  @import '../assets/style/mixins.scss';

  .container {
    background-color: $dark;
    padding-top:62px;
    padding-bottom: 30px;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    .box-card {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }
    .current-series {
      @include buttonMain();
      font-size: 22px;
      position: absolute;
      left: 300px;
      top: -28px
    }
    .load-more {
      @include loadBtn();
      font-size: 14px;
    }
  }
  
</style>