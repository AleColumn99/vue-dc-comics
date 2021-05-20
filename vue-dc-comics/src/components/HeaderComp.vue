<template>
  <header>

    <img src="../assets/img/dc-logo.png" alt="">

    <nav>
      <ul>
        <li v-for="(link, index) in links" :key="index">
          <a :class="{'active': link.current}" :href="link.url">{{ link.text }}</a>
        </li>
      </ul>
    </nav>

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

  header{
    text-align: center;
    /* margin-bottom: 4rem; */
  }
  ul{
    display: flex;
    justify-content: center;
    /* margin: 2rem 0; */
    a {
      text-decoration: none;
      padding: 1rem;
      transition: background 0.4s;
      &:hover,
      &.active{
        background: red
      }
      
    }
  }

</style>