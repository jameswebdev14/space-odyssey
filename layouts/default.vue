<template>
  <div>
    <div id="title_section">
      <h1 id="title">SPACE ODYSSEY</h1>
      <span id="subTitle">- a journey into space</span>
    </div>
    <Nav></Nav>
    <nuxt/>

  </div>
</template>

<script>
import Nav from "@/components/Nav";
import Footer from "@/components/Footer";

export default {
  components: { Nav, Footer }
};
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

body {
  background-color: black;
  color: #c0c0c0;
}

.silver_text {
  background-color: transparent;
  border: 2px solid #c0c0c0;
}

/*****DEFAULT MOBILE VIEW*****/
#title_section {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}
#title {
  font-size: 2rem;
  color: #c0c0c0;
  margin-top: 10px;
  margin-bottom: 20px;
}
#subTitle {
  font-size: 1.2rem;
  color: #c0c0c0;
  font-style: italic;
  font-weight: 300;
}

.highlight_text {
  color: red;
  text-transform: capitalize;
}

.planet_name {
  text-transform: uppercase;
  font-weight: bold;
  font-size: 1.5rem;
  text-shadow: 0 2px red;
}

.planet {
  display: flex;
  flex-flow: column;
}

#images {
  display: flex;
  flex-flow: column;
  order: 2;
}

.planet_info {
  order: 1;
}

/*******MEDIUM VIEW******/
@media (min-width: 768px) {
  #title_section {
    justify-content: center;
    align-items: center;
    display: flex;
  }

  #title {
    font-size: 4rem;
    margin: 20px 20px 30px 0;
  }

  #subTitle {
    display: inline-block;
    font-size: 2rem;
    color: #c0c0c0;
    margin-top: 20px;
    margin-bottom: 30px;
    align-items: flex-end;
  }

  .planet {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  .planet_name {
    font-size: 2.2rem;
    text-shadow: 0 2px red;
  }

  .planet_images {
    max-width: 620px;
    margin: 25px 20px;
  }
}
</style>
