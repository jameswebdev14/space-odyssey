<template>
<div class="container-fluid">
  <section class="top_image_bar">
    <div id="image_row">
      <img src="/img/oursolarsystem.jpg" alt="Solar System" class="img-fluid">
      <img src="/img/radio-signals.jpg" alt="Extraterrestial Radio Signals" class="img-fluid">
      <img src="/img/space1.jpeg" alt="Space" class="image-fluid">
      <img src="/img/earth-satellite.jpg" alt="Earth from Satelite" class="img-fluid">
      <img src="/img/solarsun.jpg" alt="Our Sun & Solar System" class="img-fluid">
      <img src="/img/spacerings.jpg" alt="Space Rings" class="img-fluid">
      <img src="/img/spiral.jpg" alt="Spiral" class="img-fluid">
      <img src="/img/space.jpg" alt="Space" class="img-fluid">
    </div>
  </section>

  <section id="intro">
      <h3>Welcome to your gateway into the mysterious and exciting world of outer space</h3>
  </section>
  <div id="main_section">
    <section id="news">
      <news v-bind:nasa_data=nasa_data></news>
    </section>
    <section id="content">
      <h5>Space trip through our solar system</h5>
      <div class="embed-responsive embed-responsive-16by9 m-auto">
        <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/m1EBHOmXSqA?rel=0&amp;controls=0&amp;showinfo=0&amp;start=32" allowfullscreen></iframe>
      </div>
    </section>
    <section id="quiz">
      <quiz></quiz>
    </section>
  </div>
</div>
</template>

<script>
import quiz from "@/components/Quiz";
import news from "@/components/News";

export default {
  name: "index",
  async asyncData({ app }) {
    const NASA_API = "moCBUS48Zn51fBuHIOMX3WlM9rUrcBDUJuz3MjN8";
    const nasa_data = await app.$axios.$get(
      `https://api.nasa.gov/planetary/apod?api_key=${NASA_API}`
    );
    console.log("nasa_data: ", nasa_data);
    return { nasa_data };
  },
  components: { quiz, news }
};
</script>

<style>
/*****DEFAULT MOBILE*****/
.container-fluid {
  min-height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: center;
}

#main_section {
  display: flex;
  flex-flow: column;
  justify-content: flex-start;
  align-items: flex-start;
  width: 100%;
}

.title {
  font-family: "montserrat", "Source Sans Pro", -apple-system,
    BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
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
  margin-top: 0;
  padding: 0 10px;
  margin-bottom: 30px;
}

#intro h4 {
  text-align: center;
  font-weight: bold;
  font-size: 1.2rem;
}

iframe {
  width: 100%;
  height: auto;
  border: 2px ridge #526488;
  margin: auto;
  width: 650px;
}

#content {
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin: auto;
}

#content h5 {
  font-size: 1.2rem;
  margin-bottom: 20px;
  color: #c0c0c0;
  text-shadow: 2px 0 red;
  letter-spacing: 2px;
}

#content div {
  display: flex;
  align-items: flex-start;
  justify-content: center;
}

.top_image_bar {
  display: none;
}

#news {
  order: 2;
  margin-top: 40px;
}

#quiz {
  margin: auto;
  margin-top: 30px;
  order: 3;
}

/*****MEDIUM UP********/
@media screen and (min-width: 991px) and (max-width: 1450px) {
  .container-fluid {
    padding: 0 30px;
  }

  .top_image_bar {
    display: block;
    max-width: 100vw;
    overflow: hidden;
    z-index: 40;
  }

  #image_row {
    display: flex;
    justify-content: center;
    position: absolute;
    top: 250px;
    left: 0;
    height: 160px;
    width: 100vw;
    border-top: 5px ridge grey;
    border-bottom: 5px ridge grey;
  }

  #image_row img {
    height: 150px;
    max-width: 12.5%;
    width: 12.5%;
    overflow: hidden;
  }

  #intro {
    color: #c0c0c0;
    text-align: center;
    width: 100%;
    margin-top: 200px;
    height: 80px;
  }

  #main_section {
    margin-top: 0;
    width: 100%;
    display: grid;
    grid-gap: 10px;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: auto auto;
    justify-content: center;
    align-items: start;
  }

  #intro h4 {
    text-align: center;
    font-weight: bold;
    font-size: 1.6rem;
  }

  #content {
    grid-row: 1 / 2;
    grid-column: 2 / 3;
    align-items: flex-start;
    justify-content: flex-start;
    width: 80%;
    margin: 40px auto;
  }

  #content h5 {
    font-size: 1.7rem;
    margin-bottom: 0;
    letter-spacing: 2px;
  }

  #quiz {
    grid-row: 2 / 3;
    grid-column: 1 / -1;
  }

  #news {
    grid-row: 1 / 2;
    grid-column: 1 / 2;
  }

  iframe {
    max-width: 600px;
    width: 100%;
    margin: auto;
    margin-top: 20px;
  }
}

/*  LARGE SCREENS  */
@media screen and (min-width: 1451px) {
  #main_section {
    margin-top: 0;
    padding-top: 0;
    width: 100%;
    display: grid;
    grid-gap: 10px;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: auto;
    justify-content: start;
    align-items: start;
  }

  .top_image_bar {
    display: block;
    margin-bottom: 150px;
  }

  #image_row {
    display: flex;
    justify-content: center;
    position: absolute;
    top: 250px;
    left: 0;
    height: 160px;
    width: 100vw;
    border-top: 5px ridge grey;
    border-bottom: 5px ridge grey;
  }

  #image_row img {
    height: 150px;
    max-width: 12.5%;
    width: 12.5%;
    overflow: hidden;
  }

  #content {
    align-items: center;
    justify-content: center;
    width: 100%;
    margin: 0;
    padding-top: 40px;
  }

  #content h5 {
    font-size: 1.7rem;
    margin-bottom: 20px;
  }

  #content div {
    margin-top: 0;
  }
}
</style>
