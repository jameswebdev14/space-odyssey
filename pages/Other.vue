<template>
<div id="misc">
  <section id="links">
    <ul>
      <li><nuxt-link to="Black_Holes.vue">Black Holes</nuxt-link></li>
      <li><nuxt-link to="Nebulas.vue">Nebulas</nuxt-link></li>
      <li><nuxt-link to="Gravity.vue">Gravity</nuxt-link></li>
      <li><nuxt-link to="Black_Holes.vue">Black Holes</nuxt-link></li>
      <li><nuxt-link to="Black_Holes.vue"></nuxt-link></li>
    </ul>
  </section>
  <section id="view">
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
  #links {
    flex-flow: column;
    align-items: flex-start;
    justify-content: center;
  }

  #links ul {
    margin: 0;
  }

  #links ul li {
    list-style: none;
  }
}
</style>

