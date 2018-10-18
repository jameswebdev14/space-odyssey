<template>
  <div>
    <div id="black-holes" class="misc">
      <div id="images">
        <img class="planet_images img-fluid" src="../../assets/img/blackhole/heart-of-milky-way.jpg" alt="Earth" style="float:left;">
        <img class="planet_images img-fluid"  src="../../assets/img/blackhole/star_black_hole.jpg" alt="Earth" style="float:left;">
        <img class="planet_images img-fluid"  src="../../assets/img/blackhole/distant-blackhole.jpg" alt="Earth" style="float:left;">
        <img class="planet_images img-fluid"  src="../../assets/img/blackhole/weird-light-hole.jpg" alt="Earth" style="float:left;">
      </div>
      <div class="info">
        <h5 class="planet_name">Black Holes</h5>
        <h6 class="info">

        </h6>
          <h6>
          <br><span class="highlight_text">Internal structure</span><br>

          <br><br><span class="highlight_text">Magnetic field</span><br>

          <br><br><span class="highlight_text">Earth's atmosphere</span><br>

          </h6>

      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
/*  DEFAULT MOBILE VEW */
#images {
  display: flex;
  flex-flow: column;
  order: 2;
}

.planet_images {
  margin-bottom: 20px;
}

.planet_facts {
  margin: 20px 0;
  padding-left: 0;
}
</style>
