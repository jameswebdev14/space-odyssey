<template>
<div id="misc">
  <section id="links">
    <ul>
      <li><nuxt-link to="misc/Black_Holes.vue">BLACK HOLES</nuxt-link></li>
      <li><nuxt-link to="misc/Nebulas.vue">NEBULAS</nuxt-link></li>
      <li><nuxt-link to="misc/Gravity.vue">GRAVITY</nuxt-link></li>
      <li><nuxt-link to="misc/Black_Holes.vue">Black Holes</nuxt-link></li>
      <li><nuxt-link to="misc/Black_Holes.vue"></nuxt-link></li>
    </ul>
  </section>
  <section id="view">
    <h5 id="intro">Here we look at other miscellaneous space topics that have not been discussed in detail so far</h5>
    <nuxt-child/>
  </section>
</div>
</template>

<style scoped>
/* DEFAULT MOBILE VIEW */
#misc {
  color: #c0c0c0;
}

#links {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  justify-content: center;
}

/* MEDIUM UP VIEW */
@media screen and (min-width: 991px) {
  #misc {
    display: grid;
    grid-template-columns: 200px 1fr;
  }
  #links {
    flex-flow: column;
    align-items: flex-start;
    justify-content: center;
    grid-column: 1 / 2;
    grid-row: 1 / 2;
    justify-content: start;
  }

  #links ul {
    margin: 0;
  }

  #links ul li {
    list-style: none;
  }

  #view {
    grid-column: 2 / 3;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 50px auto;
  }
}
</style>

