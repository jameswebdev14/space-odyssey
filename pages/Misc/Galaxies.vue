<template>
<div>
  <div id="galaxies" class="misc">
    <div class="title">GALAXIES</div>
    <div class="images-top">
      <div>
        <img class="image img-fluid" src="../../assets/img/galaxies/milkyway1.jpg" alt="Earth">
        <p class="highlight_text">The Milky Way - our galaxy</p>
      </div>
      <div>
        <img class="image img-fluid" src="../../assets/img/galaxies/andromeda.jpg" alt="Earth">
        <p class="highlight_text">Andromeda - our nearest neighbour</p>
      </div>
      <div>
        <img class="image img-fluid" src="../../assets/img/galaxies/planet-distant-discovery.jpg" alt="Earth">
        <p class="highlight_text">Distany Planets in a Galaxy far far away</p>
      </div>
    </div>
    <div class="info">
      <h6 class="info">
          Galaxies are sprawling space systems composed of dust, gas, and countless stars.<br>
          The number of galaxies cannot be counted—the observable universe alone may contain 100 billion. Some of these distant systems are similar to our own Milky Way galaxy, while others are quite different.<br>
          Galaxies with less than a billion stars are considered "small galaxies." In our own galaxy, the sun is just one of about 100 billion stars.<br><br>
          <span class="highlight_text">Types of Galaxies</span><br>
          Galaxies are classified into three main types: <span class="emphasis">spiral galaxies</span>, <span class="emphasis">elliptical galaxies</span>, and <span class="emphasis">irregular galaxies</span><br><br>
          <span class="emphasis">Spiral Galaxies</span><br> such as the Milky Way, consist of a flat disk with a bulging center and surrounding spiral arms. The galaxy's disk includes stars, planets, dust, and gas—all of which rotate around the galactic center in a regular manner.
          This spinning motion, at speeds of hundreds of kilometers per second, may cause matter in the disk to take on a distinctive spiral shape like a cosmic pinwheel. Some spiral galaxies obtain even more interesting shapes that earn them descriptive names, such as sombrero galaxies.
          Older stars reside in the bulge at the center of the galactic disk. Many new stars also form in spiral systems, and their disks are surrounded by a halo, which scientists believe is rich with mysterious dark matter.<br><br>
          <span class="emphasis">Elliptical Galaxies</span><br> are shaped as their name suggests.<br>They are generally round but stretch longer along one axis than along the other. They may be nearly circular or so elongated that they take on a cigarlike appearance.
          Elliptical galaxies contain many older stars, up to one trillion, but little dust and other interstellar matter. Their stars orbit the galactic center, like those in the disks of spiral galaxies, but they do so in more random directions. Few new stars are known to form in elliptical galaxies.<br>
          The universe's largest known galaxies are giant elliptical galaxies, which may be as much as two million light-years long. Elliptical galaxies may also be small, in which case they are dubbed dwarf elliptical galaxies.<br><br>
          <span class="emphasis">Irregular Galaxies</span><br>
          Galaxies that are not spiral or elliptical are called irregular galaxies.<br>Irregular galaxies appear misshapen and lack a distinct form, often because they are within the gravitational influence of other galaxies close by.<br><br>
          <span class="highlight_text">Galactic Mergers</span><br>
          Some galaxies occur alone or in pairs, but they are more often parts of larger associations known as groups, clusters, and superclusters.
          Galaxies in such groups often interact and even merge together in a dynamic cosmic dance of interacting gravity. Mergers cause gases to flow towards the galactic center, which can trigger phenomena like rapid star formation.<br>
          Our own <nuxt-link to="/milkyway">Milky Way</nuxt-link> may someday merge with the Andromeda galaxy—just two million light-years away and visible to the naked eye from Earth's Northern Hemisphere.<br>
          These intergalactic processes may be part of natural evolution by which irregular galaxies transform into one of the other shapes, and by which spiral galaxies eventually become elliptical galaxies—as scientists believe they must.<br><br>
          <span class="highlight_text">Galaxy Origins</span><br>
          Most astronomers suggest that galaxies formed shortly after a cosmic "big bang" that began the universe some 10 billion to 20 billion years ago. In the milliseconds following this explosion, clouds of gases began to coalesce, collapse, and compress under gravity to form the building blocks of galaxies.
          Scientists are divided on just how galaxies first formed. Some believe that smaller clusters of about one million stars, known as globular clusters, formed first and later gathered into galaxies. Others believe that galaxies formed first and that only later did the stars within them begin to gather into smaller clusters
        </h6>

    </div>
  </div>
</div>
</template>

<style scoped>
/* DEFAULT MOBILE VIEW */
#galaxies {
  padding: 5px;
  display: flex;
  flex-flow: column;
  align-items: center;
}

ul {
  padding: 5px;
}

li {
  margin-bottom: 10px;
}

.images {
  width:100%;
}

/*  MEDIUM UP VIEW */
@media screen and (min-width: 991px) {
  #galaxies {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 60px 450px auto;

    width:100%;
  }

  #info {
    font-size: 2rem;
    padding: 10px;
    grid-column: 1 / 2;
    grid-row: 3 / 4;
  }

  #info h6 {
    text-align: left;
  }

  .image {
    width:100%;
    max-width: 450px;
    height: 350px;
    margin-bottom: 5px;
  }

  p {
    font-size: 1.2rem;
  }
}
</style>
