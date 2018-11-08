<template>
  <div class="container moons">
    <section class="title-section">
      <h1 class="page-title">Moons </h1>
      <h3 class="page-subtitle">- companions </h3>
    </section>
    <section id="content">
      <section class="info">
        <h6>
          <span class="highlight_text">What is a Moon?</span><br>
          Planets and asteroids orbit the Sun. Moons—also known as natural satellites—orbit planets and asteroids.<br>
          Moons come in many shapes, sizes and types. Most are airless, but a few have atmospheres and even hidden oceans. There are hundreds of moons in our solar system—even a few asteroids have small companion moons.<br>
          Moons - also called natural satellites—come in many shapes, sizes and types. They are generally solid bodies, and few have atmospheres.<br>
          <figure style="float:left;">
            <img src="../assets/img/moon/moons1.png" class="img-fluid"/>
            <p class="caption">Major Moons of our Solar System</p>
          </figure>
          Most of the planetary moons probably formed from the discs of gas and dust circulating around planets in the early solar system.<br><br>
          <span class="highlight_text">How the Moons of Our Solar System Get Their Names</span><br>
          Most moons in our solar system are named for mythological characters from a wide variety of cultures. The newest moons discovered at Saturn, for example, are named for Norse gods such as Bergelmir, a giant.<br>
          Uranus is the exception. Uranus' moons are named for characters in William Shakespeare's plays so you’ll find Ophelia and Puck in orbit. Other Uranian moon names were chosen from Alexander Pope's poetry (Belinda and Ariel).
          Moons are given provisional designations such as S/2009 S1, the first satellite discovered at Saturn in 2009. The International Astronomical Union approves an official name when the discovery is confirmed.<br><br>
          <span class="highlight_text">Moons of the Inner Solar System</span><br>
          Of the terrestrial (rocky) planets of the inner solar system, neither Mercury nor Venus have any moons at all, Earth has one and Mars has its two small moons.<br>In the outer solar system, the gas giants Jupiter and Saturn and the ice giants Uranus and Neptune have numerous moons. As these planets grew in the early solar system, they were able to capture objects with their large gravitational fields.<br>
          Earth's Moon probably formed when a large body about the size of Mars collided with Earth, ejecting a lot of material from our planet into orbit. Debris from the early Earth and the impacting body accumulated to form the Moon approximately 4.5 billion years ago (the age of the oldest collected lunar rocks). Twelve American astronauts landed on the Moon during NASA's Apollo program from 1969 to 1972, studying the Moon and bringing back rock samples.
          Usually the term moon brings to mind a spherical object, like Earth's Moon. The two moons of Mars, Phobos and Deimos, are different. While both have nearly circular orbits and travel close to the plane of the planet's equator, they are lumpy and dark. Phobos is slowly drawing closer to Mars and could crash into the planet in 40 or 50 million years. Or the planet's gravity might break Phobos apart, creating a thin ring around Mars.<br><br>
          <figure style="float:right;">
            <img src="../assets/img/moon/jupiter-moons.jpg" class="img-fluid"/>
            <p class="caption">Jupiter's Moons</p>
          </figure>
          <span class="highlight_text">Moons of the Giant Planets</span><br>
          Jupiter has 79 known moons, including the largest moon in the solar system, Ganymede. Many of Jupiter's outer moons have highly elliptical orbits and orbit backwards (opposite to the spin of the planet). Saturn, Uranus and Neptune also have some irregular moons, which orbit far from their respective planets.
          Saturn has 53 known moons (plus eight more awaiting official confirmation). The chunks of ice and rock in Saturn's rings (and the particles in the rings of the other outer planets) are not considered moons, yet embedded in Saturn's rings are distinct moons or moonlets. These shepherd moons help keep the rings in line. Saturn's moon Titan, the second largest in the solar system, is the only moon with a thick atmosphere.
          In the realm of the ice giants, Uranus has 27 known moons. The inner moons appear to be about half water ice and half rock. Miranda is the most unusual; its chopped-up appearance shows the scars of impacts of large rocky bodies.
          Neptune has 13 known moons. And Neptune's moon Triton is as big as the dwarf planet Pluto and orbits backwards compared with Neptune's direction of rotation.<br><br>
          <span class="highlight_text">Moons of the Kuiper Belt</span><br>
          Pluto's large moon Charon is about half the size of Pluto. Like Earth's Moon, Charon may have formed from debris resulting from an early collision of an impactor with Pluto. In 2005, scientists using the Hubble Space Telescope to study Pluto found two additional, but very small, moons. The little moons Nix and Hydra are about two to three times as far from Pluto as Charon and roughly 5,000 times fainter than Pluto. Eris, another dwarf planet even more distant than Pluto, has a small moon of its own, named Dysnomia. Haumea, another dwarf planet, has two satellites, Hi'iaka and Namaka.
        </h6>
      </section>
      <section id="images">
        <figure class="figure1">
          <img src="../assets/img/moon/moons-origin.jpg" class="img-fluid"/>
          <p class="caption">Origin of the Moon</p>
        </figure>
        <figure class="figure1">
          <img src="../assets/img/moon/ceres-layers.png" class="img-fluid"/>
          <p class="caption">Ceres Structure</p>
        </figure>
      </section>
    </section>
  </div>
</template>


<style scoped>
/* DEFAULT MOBILE */
.container {
  color: #c0c0c0;
  padding: 0;
}

#content {
  display: flex;
  flex-flow: column;
  align-items: center;
}

#info {
  margin-bottom: 30px;
}

.info h6 {
  padding:5px;
}

#images img {
  max-width: 100%;
  margin-bottom: 0;
  margin-top: 20px;
}

#images p {
  margin-bottom: 30px;
}

.caption {
  font-size: 0.9rem;
  font-style:italic;
  text-align:center;
  margin-bottom:15px;
}

/* MEDIUM UP */
@media screen and (min-width: 991px) {
  .title-section {
    grid-column: 1 / 2;
    grid-row: 1 / 2;
    text-align: left;
    margin-bottom: 15px;
    display: flex;
    align-items:baseline;
  }

  #title {
    font-size: 2.5rem;
    color: #c0c0c0;
  }

  #subTitle {
    font-size: 1.3rem;
  }

  #images img, img {
    max-width: 500px;
    margin: auto;
    margin-bottom: 5px;
  }

  .info {
    margin-right: 25px;
  }

  .info h6 {
    text-align: left;
  }

  #images {
    width:100%;
    display:flex;
    flex-flow:row;
    justify-content: space-between;

  }

  #images figure {
    display:flex;
    flex-flow:row;
    justify-content: space-between;
  }

  #images .figure1 {
    display:flex;
    flex-flow:column;


  }
}
</style>
