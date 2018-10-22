<template>
  <div>
    <div id="black-holes" class="misc">
      <div id="title">BLACK HOLES</div>
      <div class="images">
        <img class="image img-fluid" src="../../assets/img/blackhole/heart-of-milky-way.jpg" alt="Earth">
        <img class="image img-fluid" src="../../assets/img/blackhole/star_black_hole.jpg" alt="Earth">
        <img class="image img-fluid" src="../../assets/img/blackhole/black-hole-event-horizon.jpg" alt="Earth">
      </div>
      <div class="info">
        <h6 class="info">
          Black holes are the strangest objects in the Universe.<br>A black hole does not have a surface, like a planet or star. Instead, it is a region of space where matter has collapsed in on itself.<br>
          Most galaxies, including the Milky Way, have supermassive black holes at their centres. These may be millions or billions of times heavier than our Sun. Supermassive black holes also power active galaxies and ancient galaxies known as quasars. Quasars may be hundreds of times brighter than even the largest ordinary galaxies.
          Objects that fall into black holes are literally stretched to breaking point. An astronaut who ventured too close and was sucked into a black hole would be pulled apart by the overpowering gravity.<br><br>
          <span class="highlight_text">How are Black Holes formed</span><br>
          This catastrophic collapse results in a huge amount of mass being concentrated in an incredibly small area. The gravitational pull of this region is so great that nothing can escape – not even light.<br>
          Because no light can get out, people can't see black holes. They are invisible. Space telescopes with special tools can help find black holes. The special tools can see how stars that are very close to black holes act differently than other stars.<br>
          Black holes come in many different sizes.
          Stellar black holes are made when the center of a very big star falls in upon itself, or collapses. When this happens, it causes a supernova. A supernova is an exploding star that blasts part of the star into space.
          Scientists think supermassive black holes were made at the same time as the galaxy they are in.
          <br><br>
          <span class="highlight_text">How Big Are Black Holes?</span><br>
          Black holes can be big or small. Scientists think the smallest black holes are as small as just one atom. These black holes are very tiny but have the mass of a large mountain. Mass is the amount of matter, or "stuff," in an object.
          Another kind of black hole is called "stellar". These 'stellar-mass' black holes form when a heavyweight star, about 10 times heavier than the Sun, ends its life in a supernova explosion. What is left of the star – still several solar masses - collapses into an area only a few kilometres across.<br>
          Its mass can be up to 20 times more than the mass of the sun. There may be many, many stellar mass black holes in Earth's galaxy. Earth's galaxy is called the Milky Way.
          The largest black holes are called "supermassive." These black holes have masses that are more than 1 million suns together. Scientists have found proof that every large galaxy contains a supermassive black hole at its center. The supermassive black hole at the center of the Milky Way galaxy is called Sagittarius A. It has a mass equal to about 4 million suns and would fit inside a very large ball that could hold a few million Earths.
          Scientists think the smallest black holes formed when the universe began.
          If Black Holes Are "Black," How Do Scientists Know They Are There?
          A black hole can not be seen because strong gravity pulls all of the light into the middle of the black hole. But scientists can see how the strong gravity affects the stars and gas around the black hole. Scientists can study stars to find out if they are flying around, or orbiting, a black hole.
          When a black hole and a star are close together, high-energy light is made. This kind of light can not be seen with human eyes. Scientists use satellites and telescopes in space to see the high-energy light.
          Could a Black Hole Destroy Earth?
          Black holes do not go around in space eating stars, moons and planets. Earth will not fall into a black hole because no black hole is close enough to the solar system for Earth to do that.
          Even if a black hole the same mass as the sun were to take the place of the sun, Earth still would not fall in. The black hole would have the same gravity as the sun. Earth and the other planets would orbit the black hole as they orbit the sun now.
          The sun will never turn into a black hole. The sun is not a big enough star to make a black hole.
        </h6>
      </div>
      <div class="images">
        <img class="image img-fluid" src="../../assets/img/blackhole/distant-blackhole.jpg" alt="Earth">
        <img class="image img-fluid" src="../../assets/img/blackhole/weird-light-hole.jpg" alt="Earth">
        <img class="image img-fluid" src="../../assets/img/blackhole/black-hole-event.jpg" alt="Earth">
      </div>
      <section class="video">
        <iframe width="660" height="400" src="https://www.youtube.com/embed/e-P5IFTqB98?controls=0&amp;start=4" frameborder="0" allow="autoplay; encrypted-media" class="embed-responsive" allowfullscreen></iframe>
        <iframe width="660" height="400" src="https://www.youtube-nocookie.com/embed/yWO-cvGETRQ?controls=0&amp;start=612" frameborder="0" allow="autoplay; encrypted-media" class="embed-responsive" allowfullscreen></iframe>
      </section>
    </div>

  </div>
</template>

<script>
export default {};
</script>

<style>
/*  DEFAULT MOBILE VEW */
#black-holes {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-flow: column;
  padding: 5px;
}

ul {
  margin: 0;
}

li {
  list-style: none;
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

.video iframe {
  display: none;
}

/* MEDIUM UP */
@media screen and (min-width: 991px) {
  #black-holes {
    display: grid;
    grid-template-columns: 1fr 2fr 1fr;
    grid-template-rows: 80px auto 500px;
    align-items: start;
  }

  #title {
    grid-column: 1 / -1;
    font-size: 1.5rem;
    margin-bottom: 15px;
    text-align: left;
  }

  #info {
    font-size: 2rem;
    padding: 10px;
  }

  .image {
    margin-bottom: 30px;
  }

  .video {
    grid-column: 1 / -1;
    display: flex;
  }

  .video iframe {
    margin: 30px;
    width: 660;
    height: 400;
  }
}
</style>
