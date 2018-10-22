<template>
<div class="b.container fluid">
  <section class="top_image_bar">
    <div id="image_row">
      <img src="/img/oursolarsystem.jpg" alt="Solar System" class="img-fluid">
      <img src="/img/radio-signals.jpg" alt="Extraterrestial Radio Signals" class="img-fluid">
      <img src="/img/space1.jpeg" alt="Space" class="image-fluid">
      <img src="/img/earth-satellite.jpg" alt="Earth from Satelite" class="img-fluid">
      <img src="/img/solarsun.jpg" alt="Our Sun & Solar System" class="img-fluid">
      <img src="/img/spacerings.jpg" alt="Space Rings" class="img-fluid">
      <img src="/img/spiral.jpg" alt="Spiral" class="img-fluid">
      <img src="/img/space.jpg" alt="" class="img-fluid">
    </div>
  </section>
  <div id="main_section">
    <section id="intro">
      <h4>Welcome to your gateway into the mysterious and exciting world of outer space</h4>
    </section>
    <section id="content">
      <iframe src="https://www.youtube.com/embed/m1EBHOmXSqA?rel=0&amp;controls=0&amp;showinfo=0&amp;start=32" frameborder="0" controls allow="autoplay; encrypted-media" class="embed-responsive"></iframe>
    </section>
    <section id="links"></section>
  </div>
</div>
</template>

<script>
export default {
  components: {}
};
</script>

<style>
/*****DEFAULT MOBILE*****/
#main_section {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
}
.fluid {
  min-height: 100vh;
  display: flex;
  justify-content: center;
}
.title {
  font-family: 'montserrat', "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 1rem;
  color: #35495e;
  letter-spacing: 1px;
}

#intro {
  color: #c0c0c0;
  justify-content: center;
  align-content: center;
  margin-top: 40px;
  padding: 0 10px;
}

#intro h4 {
  text-align: center;
  font-weight: bold;

}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links {
  padding-top: 15px;
}

#image_row {
  display: none;
}

iframe {
  width: 100%;
  height: 400px;
  border: 2px ridge #526488;
}

/*****MEDIUM UP********/
@media screen and (min-width: 768px) {
  .fluid {
    padding: 0 40px;
  }

  #main_section {
    margin-top: 170px;
    display: grid;
    grid-gap: 20px;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 50px auto;
    justify-content: start;
    align-content:start;
  }

  .top_image_bar {
    height: 180px;
  }

  #image_row {
    display: flex;
    justify-content: center;
    position: absolute;
    top: 260px;
    left: 0;
    height: 160px;
    width: 100%;
    border-top: 5px ridge grey;
    border-bottom: 5px ridge grey;
  }

  #image_row img {
    height: 150px;
    max-width: 12%;
    min-width: 13%;
  }

  #intro {
    color: #c0c0c0;
    text-align: center;
    margin-top: 20px;
    padding: 0 40px;
    grid-column: 1 / 3;
    grid-row: 1 / 2;
  }

  #content {
    display: grid;
    grid-row: 2 / 3;
    grid-column: 1 / -1;
  }

  #links {
    grid-row: 2 / 3;
    grid-column: 2 / 3;
  }

  iframe {
    width: 760px;
    height: 550px;
  }
}
</style>
