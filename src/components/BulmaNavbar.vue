<template>
  <nav class="nav has-shadow">
    <div class="nav-left">
      <a class="nav-item is-brand" href="#">
        <img src="http://bulma.io/images/bulma-type.png" alt="Bulma logo">
      </a>
    </div>

    <div class="nav-center">
      <a class="nav-item" href="#">
        <span class="icon">
          <i class="fa fa-github"></i>
        </span>
      </a>
      <a class="nav-item" href="#">
        <span class="icon">
          <i class="fa fa-twitter"></i>
        </span>
      </a>
    </div>

    <span class="nav-toggle" :class="{ 'is-active' : isMenuActive }" @click="handleMenu">
      <span></span>
      <span></span>
      <span></span>
    </span>

    <div class="nav-right nav-menu" :class="{ 'is-active' : isMenuActive }">
      <a class="nav-item" href="#">
        Home
      </a>
      <a class="nav-item" href="#">
        Documentation
      </a>
      <a class="nav-item" href="#">
        Blog
      </a>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'bulma-navbar',
  data () {
    return {
      isActive: false
    }
  },
  methods: {
    handleMenu () {
      if (this.isActive) {
        this.isActive = false
      }else{
        this.isActive = true
      }
    }
  },
  computed: {
    isMenuActive () {
      return this.isActive
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .nav {
    padding : 10px;
  }
</style>
