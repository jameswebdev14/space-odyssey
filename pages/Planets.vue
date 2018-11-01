<template>
  <div class="b-container fluid">
    <h4 class="page-title">Planets in our solar system</h4>
    <div id="planets">
      <section>
        <ul id="planet_links">
          <li><nuxt-link to="earth">EARTH</nuxt-link></li>
          <li><nuxt-link to="jupiter">JUPITER</nuxt-link></li>
          <li><nuxt-link to="mars">MARS</nuxt-link></li>
          <li><nuxt-link to="mercury">MERCURY</nuxt-link></li>
          <li><nuxt-link to="neptune">NEPTUNE</nuxt-link></li>
          <li><nuxt-link to="pluto">PLUTO</nuxt-link></li>
          <li><nuxt-link to="saturn">SATURN</nuxt-link></li>
          <li><nuxt-link to="uranus">URANUS</nuxt-link></li>
          <li><nuxt-link to="venus">VENUS</nuxt-link></li>
        </ul>
      </section>
      <section id="planet_section">
        <nuxt-child to="earth"/>
      </section>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
/*****DEAFAULT MOBILE VIEW*****/
.fluid {
  margin: 0;
  display: flex;
  flex-flow: column;
  padding: 8px;
}

h4 {
  font-size: 1.4em;
  padding-left: 10px;
  text-transform: uppercase;
  font-weight: bold;
  text-shadow: 0 2px red;
  padding: 0;
  margin-bottom: 15px;
}

#planets {
  color: #c0c0c0;
}

#planet_links {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  padding: 0;
}

li {
  list-style: none;
  font-size: 1.2rem;
  color: #c0c0c0;
  padding: 10px;
}

#title {
  padding-left: 10px;
}

/*****MEDIUM UP VIEW*****/
@media screen and (min-width: 768px) {
  .fluid {
    display: grid;
    justify-content: left;
  }
  #planets {
    display: flex;
    align-items: flex-start;
    flex-flow: row;
    justify-content: flex-start;
  }

  #planet_links {
    margin: 0 40px 0 30px;
  }

  h4 {
    font-size: 2.2rem;
    margin-bottom: 35px;
  }
}
</style>


