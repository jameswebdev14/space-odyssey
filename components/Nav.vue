<template>
  <b-navbar toggleable="lg" type="dark" variant="faded" ml-auto>
    <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
    <b-collapse is-nav id="nav_collapse">
      <b-navbar-nav ml-auto>
        <b-nav-item href="#"><nuxt-link to="/" class="link">Home</nuxt-link></b-nav-item>
        <b-nav-item href="#"><nuxt-link to="/milkyway" class="link">The Milky Way</nuxt-link></b-nav-item>
        <b-nav-item href="#"><nuxt-link to="/planets/earth" class="link">The Planets</nuxt-link></b-nav-item>
        <b-nav-item href="#"><nuxt-link to="/solarsystem" class="link">Our Solar System</nuxt-link></b-nav-item>
        <b-nav-item href="#"><nuxt-link to="/sun" class="link">The Sun</nuxt-link></b-nav-item>
        <b-nav-item href="#"><nuxt-link to="/universe" class="link">Our Universe</nuxt-link></b-nav-item>
        <b-nav-item href="#"><nuxt-link to="/other" class="link">other</nuxt-link></b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {};
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

/*****MEDIUM - LARGE VIEW*****/
@media (min-width: 768px) {
  .link {
    color: #c0c0c0;
    font-size: 1.2rem;
    font-weight: bold;
    margin: auto;
    padding: 20px;
    height: 40px;
    width: 100px;
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

  .navbar {
    height: 100px;
    margin-top: 0;
    padding-top: 0;
  }
}
</style>
