<template>
  <div>
    <div id="title_section">
      <h1 id="main-title">SPACE ODYSSEY</h1>
      <span id="main-subTitle">- a journey into space</span>
    </div>
    <Nav></Nav>
    <nuxt/>
    <Footer/>
  </div>
</template>

<script>
import Nav from "@/components/Nav";
import Footer from "@/components/Footer";

export default {
  components: { Nav, Footer }
};
</script>
