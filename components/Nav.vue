<template>
  <b-navbar toggleable="lg" id="navbar" type="dark" variant="faded" ml-auto @click="close">
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
    <b-collapse is-nav id="nav_collapse">
      <no-ssr>
        <b-navbar-nav>
          <b-nav-item href="#"><nuxt-link to="/" class="link">Home</nuxt-link></b-nav-item>
          <b-nav-item href="#"><nuxt-link to="/planets/earth" class="link">The Planets</nuxt-link></b-nav-item>
          <b-nav-item href="#"><nuxt-link to="/solarsystem" class="link">Our Solar System</nuxt-link></b-nav-item>
          <b-nav-item href="#"><nuxt-link to="/sun" class="link">The Sun</nuxt-link></b-nav-item>
          <b-nav-item href="#"><nuxt-link to="/moons" class="link">Moons</nuxt-link></b-nav-item>
          <b-nav-item href="#"><nuxt-link to="/universe" class="link">Our Universe</nuxt-link></b-nav-item>
          <b-nav-item href="#"><nuxt-link to="/misc/asteroids" class="link">Misc</nuxt-link></b-nav-item>
        </b-navbar-nav>
      </no-ssr>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  methods: {
    close() {
      /*console.log('closing menu');
      document.getElementById("nav_collapse").setAttribute('collapsed', 'true'); */
    }
  }
};
</script>

<style>
/*****DEFAULT MOBILE VIEW*****/
.link {
  color: #c0c0c0;
  font-size: 1em;
  font-weight: bold;
  text-decoration: none;
  padding: 5px;
}

.link:hover {
  color: orange;
  text-decoration: none;
  border-bottom: 5px ridge grey;
  border-radius: 2px;
}

.nuxt-link-exact-active {
  color: red;
}

#navbar {
  margin-bottom: 25px;
  margin-top:20px;
}

/*****MEDIUM - LARGE VIEW*****/
@media (min-width: 991px) {
  .link {
    color: #c0c0c0;
    font-size: 1rem;
    font-weight: bold;
    margin: auto;
    margin-bottom: 40px;
    padding: 20px;
    height: 30px;
    text-align: center;
    box-sizing: border-box;
  }

  .nuxt-link-exact-active {
    color: red;
  }

  .nuxt-link {
    margin: 0;
    padding: 0;
  }
  .navbar-nav {
    display: flex;
    justify-content: center;
    margin: auto;
  }

  #navbar {
    height: 50px;
    margin-top: 30px;
    padding-top: 0;
  }
}
</style>
