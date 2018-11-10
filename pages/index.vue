<template>
<div class="container-fluid main">
  <section class="top_image_bar puff-in-center">
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
    <section id="news" class="slide-in-bottom">
      <news v-bind:nasa_data=nasa_data></news>
    </section>
    <section id="content" class="swing-in-left-bck">
      <h5>Enjoy a space trip through our solar system</h5>
      <div class="embed-responsive embed-responsive-16by9 m-auto">
        <iframe class="embed-responsive-item" title="Journey through the solar system" src="https://www.youtube.com/embed/m1EBHOmXSqA?rel=0&amp;controls=0&amp;showinfo=0&amp;start=32" allowfullscreen></iframe>
      </div>
    </section>
    <section id="quiz" class="swing-in-right-bck">
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
    return { nasa_data };
  },
  components: { quiz, news }
};
</script>

<style>
/*****DEFAULT MOBILE*****/
.main {
  min-height: 100vh;
  display: flex;
  flex-flow: column;
  justify-content: center;
}

#main_section {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: flex-start;
  width: 100%;
}

#intro {
  color: #c0c0c0;
  justify-content: center;
  align-content: center;
  margin-top: 0;
  padding: 0 10px;
  margin-bottom: 30px;
}

#intro h3 {
  text-align: center;
  font-weight: bold;
  font-size: 1.3rem;
  text-shadow: 1px 1px red;
}

iframe {
  width: 100%;
  height: auto;
  border: 2px ridge #526488;
  margin: auto;
  width: 650px;
}

#news {
  order: 2;
  margin-top: 40px;
  width: 100%;
  padding: 0 10px 10px 10px;
}

#quiz {
  margin-top: 15px;
  order: 3;
  width:100%;
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

.puff-in-center {
	-webkit-animation: puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both;
	        animation: puff-in-center 0.7s cubic-bezier(0.470, 0.000, 0.745, 0.715) both;
}

/**
 * ----------------------------------------
 * animation puff-in-center
 * ----------------------------------------
 */
@-webkit-keyframes puff-in-center {
  0% {
    -webkit-transform: scale(2);
            transform: scale(2);
    -webkit-filter: blur(2px);
            filter: blur(2px);
    opacity: 0;
  }
  100% {
    -webkit-transform: scale(1);
            transform: scale(1);
    -webkit-filter: blur(0px);
            filter: blur(0px);
    opacity: 1;
  }
}
@keyframes puff-in-center {
  0% {
    -webkit-transform: scale(2);
            transform: scale(2);
    -webkit-filter: blur(2px);
            filter: blur(2px);
    opacity: 0;
  }
  100% {
    -webkit-transform: scale(1);
            transform: scale(1);
    -webkit-filter: blur(0px);
            filter: blur(0px);
    opacity: 1;
  }
}





/*****MEDIUM UP********/
@media screen and (min-width: 991px) and (max-width: 1450px) {
  .main {
    padding: 10px;
    display:grid;
    grid-template-rows: 160px 100px auto;

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
    height: 150px;
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
    margin-top: 80px;
    margin-bottom:30px;
    height: 80px;
  }

  #main_section {
    margin-top: 90px;
    padding:20px;
    width: 100%;
    display: grid;
    grid-gap: 10px;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: auto auto;
    justify-content: start;
    align-items: start;
  }

  #intro h3 {
    text-align: center;
    font-weight: bold;
    font-size: 1.8rem;
    text-shadow: 1px 1px red;

  }

  #content {
    grid-row: 1 / 2;
    grid-column: 1 / 3;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;

    background-color: rgba(0, 0, 0, 0.5);
  }

  #content h5 {
    font-size: 1.7rem;
    margin-bottom: 0;
    letter-spacing: 2px;
  }

  #content div {
    margin: auto;
  }

  #quiz {
    grid-row: 2 / 3;
    grid-column: 2 / -1;
    margin: 0 auto;
    width:100%;
    padding: 0 15px 15px 15px;
  }

  #news {
    grid-row: 2 / 3;
    grid-column: 1 / 2;
    margin: 0 auto;
    padding: 0 15px 15px 15px;
  }

  iframe {
    width: 100%;
    margin: auto;
    margin-top: 20px;
  }

}

/*  LARGE SCREENS  */
@media screen and (min-width: 1451px) {
  .main {
    padding: 0 30px;
    display:grid;
    grid-template-rows: 200px 100px auto;
  }

  #main_section {
    margin-top: 0;
    padding: 0 40px;
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
  }

  #image_row {
    display: flex;
    justify-content: center;
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

  #news {
    margin: 0;
    width:100%;
    padding: 0 15px 15px 15px;
  }

  #quiz {
    margin: 0;
    width:100%;
    padding: 0 15px 15px 15px;
  }

  #content {
    align-items: center;
    justify-content: center;
    margin: 0;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.5);
  }

  #content h5 {
    font-size: 1.7rem;
    padding-bottom: 20px;
  }

  #content div {
    margin-top: 0;
  }

  #intro h3 {
    text-align: center;
    font-weight: bold;
    font-size: 2rem;
    /*text-shadow: 2px 2px red;*/
    color: black;
    letter-spacing: 3px;
    text-shadow: -1px -1px 0 red, 1px -1px 0 red, -1px 1px 0 red, 1px 1px 0 red;
  }


}
</style>
