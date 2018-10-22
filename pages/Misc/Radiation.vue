<template>
  <div id="radiation">
    <div id="title">SOLAR RADIATION</div>
    <div class="images">
      <img class="image img-fluid" src="../../assets/img/radiation/Spectrum-of-solar-radiation.png" alt="Radiation Spectrum">
      <img class="image img-fluid" src="../../assets/img/radiation/energy_balance.jpg" alt="Energy Balance">
      <img class="image img-fluid" src="../../assets/img/radiation/global_warming_en.jpg" alt="Global Warming">
    </div>
    <div class="info">
      <h6 class="info">
        Sunlight is a portion of the electromagnetic radiation given off by the Sun, in particular infrared, visible, and ultraviolet light.<br>On Earth, sunlight is filtered through Earth's atmosphere, and is obvious as daylight when the Sun is above the horizon.<br>
        When the direct solar radiation is not blocked by clouds, it is experienced as sunshine, a combination of bright light and radiant heat. When it is blocked by clouds or reflects off other objects, it is experienced as diffused light. The World Meteorological Organization uses the term "sunshine duration" to mean the cumulative time during which an area receives direct irradiance from the Sun of at least 120 watts per square meter.<br>
        Other sources indicate an "Average over the entire earth" of "164 Watts per square meter over a 24 hour day".Sunlight is a portion of the electromagnetic radiation given off by the Sun, in particular infrared, visible, and ultraviolet light. On Earth, sunlight is filtered through Earth's atmosphere, and is obvious as daylight when the Sun is above the horizon. When the direct solar radiation is not blocked by clouds, it is experienced as sunshine, a combination of bright light and radiant heat. When it is blocked by clouds or reflects off other objects, it is experienced as diffused light. The World Meteorological Organization uses the term "sunshine duration" to mean the cumulative time during which an area receives direct irradiance from the Sun of at least 120 watts per square meter. Other sources indicate an "Average over the entire earth" of "164 Watts per square meter over a 24 hour day".<br>
        The ultraviolet radiation in sunlight has both positive and negative health effects, as it is both a principal source of vitamin D3 and a mutagen.<br>
        Sunlight takes about 8.3 minutes to reach Earth from the surface of the Sun. A photon starting at the center of the Sun and changing direction every time it encounters a charged particle would take between 10,000 and 170,000 years to get to the surface.<br><br>
        The spectrum of the Sun's solar radiation is close to that of a black body with a temperature of about 5,800 K. The Sun emits EM radiation across most of the electromagnetic spectrum. Although the Sun produces gamma rays as a result of the nuclear-fusion process, internal absorption and thermalization convert these super-high-energy photons to lower-energy photons before they reach the Sun's surface and are emitted out into space. As a result, the Sun does not emit gamma rays from this process, but it does emit gamma rays from solar flares.[12] The Sun also emits X-rays, ultraviolet, visible light, infrared, and even radio waves;[13] the only direct signature of the nuclear process is the emission of neutrinos.<br>
        Although the solar corona is a source of extreme ultraviolet and X-ray radiation, these rays make up only a very small amount of the power output of the Sun (see spectrum at right). The spectrum of nearly all solar electromagnetic radiation striking the Earth's atmosphere spans a range of 100 nm to about 1 mm (1,000,000 nm).<br><br|>
        This band of significant radiation power can be divided into five regions in increasing order of wavelengths:<br><br>
        <ul>
          <li><span class="highlight_text">Ultraviolet C or (UVC)</span> range, which spans a range of 100 to 280 nm. The term ultraviolet refers to the fact that the radiation is at higher frequency than violet light (and, hence, also invisible to the human eye). Due to absorption by the atmosphere very little reaches Earth's surface. This spectrum of radiation has germicidal properties, as used in germicidal lamps.</li><br>
          <li><span class="highlight_text">Ultraviolet B or (UVB)</span> range spans 280 to 315 nm. It is also greatly absorbed by the Earth's atmosphere, and along with UVC causes the photochemical reaction leading to the production of the ozone layer. It directly damages DNA and causes sunburn, but is also required for vitamin D synthesis in the skin and fur of mammals.</li><br>
          <li><span class="highlight_text">Ultraviolet A or (UVA)</span> spans 315 to 400 nm. This band was once held to be less damaging to DNA, and hence is used in cosmetic artificial sun tanning (tanning booths and tanning beds) and PUVA therapy for psoriasis. However, UVA is now known to cause significant damage to DNA via indirect routes (formation of free radicals and reactive oxygen species), and can cause cancer.</li><br>
          <li><span class="highlight_text">Visible range or light</span> spans 380 to 780 nm. As the name suggests, this range is visible to the naked eye. It is also the strongest output range of the Sun's total irradiance spectrum.</li><br>
          <li><span class="highlight_text">Infrared range</span> that spans 700 nm to 1,000,000 nm (1 mm). It comprises an important part of the electromagnetic radiation that reaches Earth. Scientists divide the infrared range into three types on the basis of wavelength: Infrared-A: 700 nm to 1,400 nm
        Infrared-B: 1,400 nm to 3,000 nm
        Infrared-C: 3,000 nm to 1 mm.</li><br>
        </ul>
        
        
        
      </h6>
    </div>
  </div>
</template>



<style scoped>
/* DEFAULT MOBILE VIEW */
#radiation {
  display: flex;
  flex-flow: column;
}

.image {
  width: 95%;
  margin: auto;
}

li {
  list-style: none;
  font-style:italic;
}
/* MEDIUM UP VIEW */
@media screen and (min-width: 991px) {
  #radiation {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 80px 400px auto;
  }

  #title {
    grid-column: 1 / -1;
    font-size: 1.5rem;
    text-align:left;
  }

  .images {
    display: flex;
    justify-content: space-evenly;
  }

  .image {
    width: 30%;
    grid-column: 1 / -1;
    grid-row: 2 / 3;
    height: 350px;
  }

  .info {
    grid-row: 3 / 4;
    grid-column: 1 / 2;
  }

  .info h6 {
    text-align:left;
  }
}
</style>
