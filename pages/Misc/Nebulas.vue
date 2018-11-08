<template>
  <div id="nebula">
    <div class="title">NEBULA</div>
    <div class="images-top">
      <div>
        <img class="image img-fluid" src="../../assets/img/nebula/eagle-nebula.jpg" alt="The Eagle Nebula">
        <p class="highlight_text">The Eagle Nebula</p>
      </div>
      <div>
        <img class="image img-fluid" src="../../assets/img/nebula/hubble-nebula-image.jpg" alt="The Helix Nebula">
        <p class="highlight_text">Hubble Nebula Image</p>
      </div>
      <div>
        <img class="image img-fluid" src="../../assets/img/nebula/nebula-collection.jpg" alt="Nebula Collection">
        <p class="highlight_text">Collection of some known Nebula</p>
      </div>
    </div>
    <div class="info">
      <h6 class="info">
          A nebula is a giant cloud of dust and gas in space. Some nebulae (more than one nebula) come from the gas and dust thrown out by the explosion of a dying star, such as a supernova.<br>
          Other nebulae are regions where new stars are beginning to form.<br>
          For this reason, some nebulae are called "star nurseries."<br><br>
          Nebulae are made of dust and gases—mostly hydrogen and helium. The dust and gases in a nebula are very spread out, but gravity can slowly begin to pull together clumps of dust and gas. As these clumps get bigger and bigger, their gravity gets stronger and stronger.<br><br>
          <span class="highlight_text">How do stars form in a Nebula?</span><br>
          Eventually, the clump of dust and gas gets so big that it collapses from its own gravity. The collapse causes the material at the center of the cloud to heat up-and this hot core is the beginning of a star.<br><br>
          <span class="highlight_text">Where are Nebulae?</span><br>
          Nebulae exist in the space between the stars—also known as interstellar space.<br>The closest known nebula to Earth is called the Helix Nebula (see image).
          <figure style="max-width:400px; float:right;">
              <img src="../../assets/img/nebula/helix-nebula.jpg" alt="Helix Nebula" class="img-fluid">
              <figcaption>Helix Nebula</figcaption>
          </figure><br>
          The famous Eagle nebula has structures known as Pillars of Creation because those pillar-like structures give birth to new stars. The Eagle nebula is also known as Star Queen Nebula and is located in Serpens constellation.<br>
          That means even if you could travel at the speed of light, it would still take you 700 years to get there! <br><br>
          <span class="highlight_text">How do we know what nebulae look like?</span>
          Astronomers use very powerful telescopes to take pictures of faraway nebulae. Space telescopes such as NASA's Spitzer Space Telescope and Hubble Space Telescope have captured many images of faraway nebulae.


      </h6>
    </div>
  </div>
</template>

<style scoped>
/* DEFAULT MOBILE VIEW */
#nebula {
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

#info {
  font-size: 1rem;
  padding: 5px;
}

.images-top div {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
}

/*  MEDIUM UP VIEW */
@media screen and (min-width: 991px) {
  #nebula {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 60px 500px auto;
    align-items: start;
  }

  #info {
    font-size: 2rem;
    padding: 10px;
    grid-column: 1 / -1;
    grid-row: 3 / 4;
    width: 100%;
  }

  #info h6 {
    text-align: left;
  }

  .image {
    width:100%;
    height: 420px;
    max-width: 450px;
    max-height: 450px;
  }

  p {
    font-size: 1.2rem;
  }
}
</style>

