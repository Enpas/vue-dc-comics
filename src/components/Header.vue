<template>
  <header>

    <div class="container">

      <a href="/"><img src="../assets/img/dc-logo.png" alt="Logo"></a>

      <ul>
        <li v-for="(link, index) in links" :key="index" :class="{'active': link.current === true}">
          <a href="link.url" :class="{'active': link.current === true}">{{link.text}}</a>
        </li>
      </ul>

    </div>

  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      links: [
        {
          text: 'Charachters',
          url: '#',
          current: false
        },
        {
          text: 'Comics',
          url: '#',
          current: true
        },
        {
          text: 'Movies',
          url: '#',
          current: false
        },
        {
          text: 'Tv',
          url: '#',
          current: false
        },
        {
          text: 'Games',
          url: '#',
          current: false
        },
        {
          text: 'Collectibles',
          url: '#',
          current: false
        },
        {
          text: 'Videos',
          url: '#',
          current: false
        },
        {
          text: 'Fans',
          url: '#',
          current: false
        },
        {
          text: 'News',
          url: '#',
          current: false
        },
        {
          text: 'Shop',
          url: '#',
          current: false
        }
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
  @import '../assets/style/vars.scss';
  
  .container {
    display: flex;
    height: 131px;
    justify-content: space-between;
    align-items: center;
    img {
      height: 85px;
    }
    ul {
      display: flex;
      height: 131px;
      li {
        margin: 0 10px;
        &.active {
          border-bottom: 5px solid $light-blue;
        }
      }
      a {
        display: inline-block;
        color: $dark;
        text-transform: uppercase;
        font-weight: bold;
        font-size: 12px;
        line-height: 117px;
        &.active {
          color: $light-blue;
        }
      }
    }
  }
</style>