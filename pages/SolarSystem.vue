<template>
  <div class="container">
    <section id="solar_system">
      <section id="solar_system_text">
        <h5>The solar system is made up of the sun and everything that orbits around it, including planets, moons, asteroids,
        comets and meteoroids. It extends from the sun, called Sol by the ancient Romans, and goes past the four inner planets,
        through the Asteroid Belt to the four gas giants and on to the disk-shaped Kuiper Belt and far beyond to the teardrop-shaped heliopause. Scientists estimate that the edge of the solar system is about 9 billion miles (15 billion kilometers) from the sun.
        Beyond the heliopause lies the giant, spherical Oort Cloud, which is thought to surround the solar system<br><br>
        <strong class="highlight_text">Formation</strong><br>
        Many scientists think our solar system formed from a giant,
        rotating cloud of gas and dust known as the solar nebula. As the nebula collapsed because of its gravity,
        it spun faster and flattened into a disk. Most of the material was pulled toward the center to form the sun.
        Other particles within the disk collided and stuck together to form asteroid-sized objects named as planetesimals,
        some of which combined to become the asteroids, comets, moons and planets.<br>
        The solar wind from the sun was so powerful that it swept away most of the lighter elements, such as hydrogen and helium, from the innermost planets, leaving behind mostly small, rocky worlds. The solar wind was much weaker in the outer regions, however, resulting in gas giants made up mostly of hydrogen and helium.
        The <nuxt-link to="sun">sun</nuxt-link> is by far the largest object in our solar system, containing 99.8 percent of the solar system's mass. It sheds most of the heat and light that makes life possible on Earth and possibly elsewhere. Planets orbit the sun in oval-shaped paths called ellipses, with the sun slightly off-center of each ellipse.
        NASA has a fleet of spacecraft observing the sun to learn more about its composition,
        and to make better predictions about solar activity and its effect on Earth.<br>
        The four inner four planets — Mercury, Venus, Earth and Mars — are made up mostly of iron and rock. They are known as terrestrial or earthlike planets because of their similar size and composition.
        Earth has one natural satellite — the moon — and Mars has two moons — Deimos and Phobos.
        Between Mars and Jupiter lies the <nuxt-link to='../other/asteroid-belt'>Asteroid Belt</nuxt-link>. Asteroids are minor planets, and scientists estimate there are more than 750,000 of them with diameters larger than three-fifths of a mile (1 km) and millions of smaller asteroids. The dwarf planet Ceres, about 590 miles (950 km) in diameter, resides here. A number of asteroids have orbits that take them closer into the solar system that sometimes lead them to collide with Earth or the other inner planets.</h5>
      </section>
      <div  id="images">
        <img src="../assets/img/solar.jpg" alt="Solar System" class="img-fluid">
        <img src="../assets/img/beyond_solar.jpg" alt="Solar System" class="img-fluid">
      </div>
    </section>
  </div>
</template>

<style scoped>
/* DEFAULT MOBILE VIEW */
#solar_system {
  display:flex;
  flex-flow: column;
  justify-content:center;
}

#solar_system_text {
  padding:5px;
}

#solar_system_text h5 {
  font-size:1rem;
}

#solar_system_img {
  display:flex;
  flex-wrap:wrap;
  justify-content: center;
  align-items:center;
  margin-bottom:20px;
}

img {
  max-width:700px;
}

/*  MEDIUM UP VIEW */
@media screen and (min-width:991px) {
#solar_system {
  flex-flow: row;
  justify-content:center;
  align-items: center;
}

#solar_system_text {
  margin: auto;
  padding:30px;
  font-size: 2rem;
}

#solar_system_img {
  display:flex;
  justify-content: space-evenly;
  margin-bottom:40px;
}

#solar_system_text h4 {
  font-size: 1.5rem;
  margin-bottom:20px;
}

#images img {
    max-width: 500px;
    margin-bottom:30px;
  }
}

</style>
