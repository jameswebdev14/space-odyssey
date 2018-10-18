<template>
  <div class="container">
    <section id="title-section">
      <h1 id="title">The Milky Way</h1>
      <h3 id="subTitle"> - Home Sweet Home</h3>
    </section>
    <section id="content">
      <section id="info">
      <h5>The Milky Way Galaxy is most significant to humans because it is home sweet home. But when it comes down to it, our galaxy is a typical barred spiral, much like billions of other galaxies in the universe.<br>Let's take a look at the Milky Way.<br>Our local Orion Arm of the Milky Way is some 3,500 light years across. It's approximately 10,000 light years in length. Our sun, the Earth, and all the other planets in our solar system reside within this Orion Arm.<br>
      We're located close to the inner rim of this spiral arm, about halfway along its length.<br>
      The Milky Way is a barred spiral galaxy, about 100,000 light-years across. If you could look down on it from the top, you would see a central bulge surrounded by four large spiral arms that wrap around it.<br>
      Spiral galaxies make up about two-third of the galaxies in the universe.<br>
      Unlike a regular spiral, a barred spiral contains a bar across its center region, and has two major arms. The Milky Way also contains two significant minor arms, as well as two smaller spurs. One of the spurs, known as the Orion Arm, contains the sun and the solar system.<br>
      The Orion arm is located between two major arms, Perseus and Sagittarius.<br>
      The Milky Way does not sit still, but is constantly rotating. As such, the arms are moving through space. The sun and the solar system travel with them. The solar system travels at an average speed of 515,000 mph (828,000 km/h). Even at this rapid speed, the solar system would take about 230 million years to travel all the way around the Milky Way.<br>
      Our galaxy is surrounded by an enormous halo of hot gas that extends for hundreds of thousands of light-years. The gas halo is estimated to be as massive as all of the stars in the Milky Way. Like the galaxy itself, the halo is spinning rapidly.<br>
      Curled around the center of the galaxy, the spiral arms contain a high amount of dust and gas. New stars are constantly formed within the arms. These arms are contained in what is called the disk of the galaxy. It is only about 1,000 light-years thick.<br>
      At the center of the galaxy is the galactic bulge. The heart of the Milky Way is crammed full of gas, dust, and stars. The bulge is the reason that you can only see a small percentage of the total stars in the galaxy. Dust and gas within it are so thick that you can't even peer into the bulge of the Milky Way, much less see out the other side.<br>
      Tucked inside the very center of the galaxy is a monstrous black hole, billions of times as massive as the sun. This supermassive black hole may have started off smaller, but the ample supply of dust and gas allowed it to gorge itself and grow into a giant. The greedy glutton also consumes whatever stars it can get a grip on. Although black holes cannot be directly viewed, scientists can see their gravitational effects as they change and distort the paths of the material around it, or as they fire off jets. Most galaxies are thought to have a <nuxt-link to="blackholes">black hole</nuxt-link> in their heart.<br><br>
      The bulge and the arms are the most obvious components of the Milky Way, but they are not the only pieces. The galaxy is surrounded by a spherical halo of hot gas, old stars and globular clusters. Although the halo stretches for hundreds of thousands of light-years, it only contains about two percent as many stars as are found within the disk.Scientists can't directly detect the material, but like black holes, they can measure it based on its effect on the objects around it. As such, dark matter is estimated to make up 90 percent of the mass of the galaxy.
      Recent measurements have weighed the galaxy at between 400 billion and 780 billion times the mass of the sun. By focusing on how the Milky Way affects its neighboring globular clusters, dense groups of stars smaller than a galaxy, scientists were able to calculate the mass of the Milky Way at varying distances. The result can help them improve their understanding of how much of the galaxy is made up of ordinary material like dust and stars, and how much is composed of dark matter.<br><br>
      <span class="highlight_text">Milky Way Facts</span><br>
      The Milky Way contains over 200 billion stars, and enough dust and gas to make billions more.<br>
      The solar system lies about 30,000 light-years from the galactic center, and about 20 light-years above the plane of the galaxy. Earth and its neighbors don't orbit within the plane of the galaxy but are instead tipped by about 63 degrees.
      More than half the stars found in the Milky Way are older than the 4.5-billion-year-old sun. Galaxies like ours typically undergo a stellar baby boom, churning out stars in enormous quantities roughly 10 billion years ago.
      The most common stars in the galaxy are red dwarfs, a cool star about a tenth the mass of the sun. Once thought unsuitable for potential life-bearing planets because such bodies would have to be too close to meet the criteria, red dwarfs are now considered potential suspects.<br>
      As late as the 1920s, astronomers thought all of the stars in the universe were contained inside of the Milky Way. It wasn't until Edwin Hubble discovered a special star known as a Cepheid variable, which allowed him to precisely measure distances, that astronomers realized that the fuzzy patches once classified as nebula were actually separate galaxies.<br>

      </h5></section>
      <section id="images">
        <p class="highlight_text">The Arms of the Milky Way</p>
        <img src="../assets/img/milkyway/Milky_Way_Arms.png" class="img-fluid"/>
        <p class="highlight_text">Milky Way Spiral</p>
        <img src="../assets/img/milkyway/spiral.jpg" class="img-fluid"/>
        <p class="highlight_text">Milky Way pulsar</p>
        <img src="../assets/img/milkyway/milkyway_pulsar.jpeg" class="img-fluid"/>
        <p class="highlight_text">Merging of Milky Way with Andromeda</p>
        <img src="../assets/img/milkyway/merge.jpg" class="img-fluid"/>


      </section>
    </section>


  </div>
</template>


<style scoped>
/* DEFAULT MOBILE */
.container {
  color: #c0c0c0;
}

#content {
  display: flex;
  flex-flow: column;
  align-items: center;
}

#title-section {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: baseline;
}
#title {
  font-size: 1.5rem;
  margin-bottom: 5px;
}

#subTitle {
  font-size: 1rem;
  font-style: italic;
  margin-bottom: 20px;
}

#info {
  margin-bottom: 30px;
}

#info h5 {
  font-size: 1rem;
}

#images img {
  max-width: 100%;
  margin-bottom: 30px;
  margin-top: -15px;
}

/* MEDIUM UP */
@media screen and (min-width: 991px) {
  #title-section {
    margin-bottom: 40px;
  }

  #title {
    font-size: 2.5rem;
  }

  #subTitle {
    font-size: 1.3rem;
  }

  #content {
    display: flex;
    flex-flow: row;
    justify-content: center;
  }

  #images img {
    max-width: 500px;
    margin-bottom: 30px;
  }

  #info {
    order: 1;
    margin-right: 25px;
  }

  #images {
    align-self: flex-start;
    justify-items: center;
  }
}
</style>
