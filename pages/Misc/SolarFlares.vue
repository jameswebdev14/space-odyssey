<template>
<div>
  <div id="solarflares">
    <div id="title">SOLAR FLARES</span> </div>
      <div class="images">
        <img class="image img-fluid" src="../../assets/img/solarflares/solarflare4.png" alt="Earth">
        <img class="image img-fluid" src="../../assets/img/solarflares/earth-solarflare.jpg" alt="Earth">
        <img class="image img-fluid" src="../../assets/img/solarflares/solarflares2.jpg" alt="Earth">
      </div>
      <div class="info">
        <h6 class="info">
        <span class="highlight_text">What is a Solar Flare</span><br>
        A solar flare is a sudden flash of increased brightness on the Sun, usually observed near its surface and in close proximity to a sunspot group<br>
        Powerful flares are often, but not always, accompanied by a coronal mass ejection.<br><br>
        <span class="highlight_text">What causes Solar Flares</span><br>
        A solar flare occurs when magnetic energy that has built up in the solar atmosphere is suddenly released. Radiation is emitted across virtually the entire electromagnetic spectrum, from radio waves at the long wavelength end, through optical emission to x-rays and gamma rays at the short wavelength end.<br>
        The amount of energy released is the equivalent of millions of 100-megaton hydrogen bombs exploding at the same time! The first solar flare recorded in astronomical literature was on September 1, 1859.<br>
        Two scientists, Richard C. Carrington and Richard Hodgson, were independently observing sunspots at the time, when they viewed a large flare in white light.<br>
        As the magnetic energy is being released, particles, including electrons, protons, and heavy nuclei, are heated and accelerated in the solar atmosphere. The energy released during a flare is typically on the order of 1027 ergs per second. Large flares can emit up to 1032 ergs of energy. This energy is ten million times greater than the energy released from a volcanic explosion. On the other hand, it is less than one-tenth of the total energy emitted by the Sun every second.
        There are typically three stages to a solar flare. First is the precursor stage, where the release of magnetic energy is triggered. Soft x-ray emission is detected in this stage. In the second or impulsive stage, protons and electrons are accelerated to energies exceeding 1 MeV. During the impulsive stage, radio waves, hard x-rays, and gamma rays are emitted. The gradual build up and decay of soft x-rays can be detected in the third, decay stage. The duration of these stages can be as short as a few seconds or as long as an hour.
        Solar flares extend out to the layer of the Sun called the corona. The corona is the outermost atmosphere of the Sun, consisting of highly rarefied gas. This gas normally has a temperature of a few million degrees Kelvin. Inside a flare, the temperature typically reaches 10 or 20 million degrees Kelvin, and can be as high as 100 million degrees Kelvin. The corona is visible in soft x-rays, as in the above image. Notice that the corona is not uniformly bright, but is concentrated around the solar equator in loop-shaped features. These bright loops are located within and connect areas of strong magnetic field called active regions. Sunspots are located within these active regions. Solar flares occur in active regions.
        The frequency of flares coincides with the Sun's eleven year cycle. When the solar cycle is at a minimum, active regions are small and rare and few solar flares are detected. These increase in number as the Sun approaches the maximum part of its cycle. The Sun will reach its next maximum in the year 2011, give or take one year.
        A person cannot view a solar flare by simply staring at the Sun. <span style="font-style:italic; color:purple; font-weight:bolder;">(NEVER LOOK DIRECTLY AT THE SUN! EYE DAMAGE CAN RESULT.)</span><br>Flares are in fact difficult to see against the bright emission from the photosphere. Instead, specialized scientific instruments are used to detect the radiation signatures emitted during a flare. The radio and optical emissions from flares can be observed with telescopes on the Earth. Energetic emissions such as x-rays and gamma rays require telescopes located in space, since these emissions do not penetrate the Earth's atmosphere. 
        </h6>
      </div>
      <section class="video">
        <iframe src="https://www.youtube.com/embed/g9owdmL2UWQ?controls=0" frameborder="0" allow="autoplay; encrypted-media" class="embed-responsive" allowfullscreen></iframe>
      </section>
  </div>
</div>
</template>



<style scoped>
/* MOBILE DEFAULT */
#solarflares {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column;
  padding: 5px;
}

#title {
  text-transform: uppercase;
  font-weight: bold;
  font-size: 1rem;
  text-shadow: 0 2px red;
  padding: 0;
  margin-bottom: 15px;
}

.image {
  margin-bottom: 15px;
}

.video {
  display:none;
}

iframe{ 
  width:100%;
}

/* MEDIUM UP VIEW */
@media screen and (min-width: 991px) {
  #solarflares {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 80px 320px auto 450px;
    justify-content: start;
    align-items: start;
  }

  #title {
    grid-column: 1 / -1;
    font-size: 1.5rem;
    margin-bottom: 15px;
    text-align: left;
  }

  .images {
    grid-template-columns: 1 / -1;
    grid-template-rows: 2 / 3;
    display: flex;
    justify-content: space-between;
    align-items:center;
  }

  #info {
    font-size: 2rem;
    padding: 10px;
    text-align:left;
    grid-template-columns: 1 / -1;
    grid-template-rows: 3 / 4;
  }

  .video {
    grid-template-columns: 1 / -1;
    grid-template-rows: 4 / 5;
  }

  .image {
    margin-bottom: 30px;
    height:300px;
    max-height:300px;
    width:30%;
  }

  iframe {
    max-width:550px;
    height:450px;
    margin:auto;
  }
}
</style>
