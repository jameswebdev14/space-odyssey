<template>
  <div class="b-container fluid">
    <h4 class="mb-3">Planets in our solar system</h4>
    <div id="planets">
      <section>
        <ul id="planet_links">
          <li><nuxt-link to="/planets/earth">EARTH</nuxt-link></li>
          <li><nuxt-link to="/planets/jupiter">JUPITER</nuxt-link></li>
          <li><nuxt-link to="/planets/mars">MARS</nuxt-link></li>
          <li><nuxt-link to="mercury">MERCURY</nuxt-link></li>
          <li><nuxt-link to="neptune">NEPTUNE</nuxt-link></li>
          <li><nuxt-link to="pluto">PLUTO</nuxt-link></li>
          <li><nuxt-link to="saturn">SATURN</nuxt-link></li>
          <li><nuxt-link to="uranus">URANUS</nuxt-link></li>
          <li><nuxt-link to="venus">VENUS</nuxt-link></li>
        </ul>
      </section>
      <section id="planet_section">
        <nuxt-child to="earth"></nuxt-child>
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
  font-size: 1.2em;
  padding-left: 10px;
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

  #planet_section {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr;
  }
}
</style>


/*
  #solar_system {

    display: flex;
    width: 100%;
    margin-bottom: 40px;
    justify-content: center;
  }

  #solar_system_img {
    margin-right: 20px;
    width: 45%;
  }

  #solar_system_text {
    width: 45%;
  }

  #planet_section {
    /* contains planet list, image and info */
    display: flex;
    flex-wrap: wrap;
  }

  .planet {
    display: flex;
    margin-bottom: 40px;
  }

  .planet img {
    flex: 1;
    padding-right: 10px;
    width: 500px;
    max-height: 600px;
  }

  .planet_info {
    flex-flow: column;
    align-items: flex-start;
    flex: 2;

    margin-bottom: 10px;
    max-height: 600px;
    overflow-y: auto;
  } */
