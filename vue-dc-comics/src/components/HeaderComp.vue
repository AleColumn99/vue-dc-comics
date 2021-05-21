<template>

  <header>

    <div class="container">

    <img src="../assets/img/dc-logo.png" alt="">

    <nav>
      <ul>
        <li v-for="(link, index) in links" :key="index" :class="{'active': link.current}">
          <a :class="{'active': link.current}" :href="link.url">{{ link.text }}</a>
        </li>
      </ul>
    </nav>

    </div>

  </header>

</template>

<script>
export default {
  name: 'HeaderComp',
  data(){
    return{
      links:[
        {
          text:'charachters',
          url: '#',
          current: false
        },
        {
          text:'comics',
          url: '#',
          current: true
        },
        {
          text:'movies',
          url: '#',
          current: false
        },
        {
          text:'tv',
          url: '#',
          current: false
        },
        {
          text:'games',
          url: '#',
          current: false
        },
        {
          text:'collectibles',
          url: '#',
          current: false
        },
        {
          text:'videos',
          url: '#',
          current: false
        },
        {
          text:'fans',
          url: '#',
          current: false
        },
        {
          text:'news',
          url: '#',
          current: false
        },
        {
          text:'shop',
          url: '#',
          current: false
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

@import '../assets/style/utilities.scss';

  header{
    height: 150px;
    div {
    display: flex;
    justify-content: space-between;
    text-align: center;
    height: 100%;
    width: 100%;
    }
    img {
      margin: 20px 0;
    }
  }
  ul{
    display: flex;
    justify-content: center;
    line-height: 120px;
    li {
      list-style: none;
      padding: 0 10px;
      text-transform: uppercase;
      &:hover,
      &.active {
        color: #0280F5;
        border-bottom: 3px solid #0280F5;
      }
    }
    a {
      text-decoration: none;
      color: black;
      height: 100%;
      &:hover,
      &.active {
        color: #0280F5;
      }
    }
  }

</style>