<template>
  <div>
    <div id="title_section" class="text-focus-in">
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

<style scoped>
@media screen and (min-width:991px) {
  .text-focus-in {
	-webkit-animation: text-focus-in 1s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
	        animation: text-focus-in 1s cubic-bezier(0.550, 0.085, 0.680, 0.530) both;
}

/**
 * ----------------------------------------
 * animation text-focus-in
 * ----------------------------------------
 */
@-webkit-keyframes text-focus-in {
  0% {
    -webkit-filter: blur(12px);
            filter: blur(12px);
    opacity: 0;
  }
  100% {
    -webkit-filter: blur(0px);
            filter: blur(0px);
    opacity: 1;
  }
}
@keyframes text-focus-in {
  0% {
    -webkit-filter: blur(12px);
            filter: blur(12px);
    opacity: 0;
  }
  100% {
    -webkit-filter: blur(0px);
            filter: blur(0px);
    opacity: 1;
  }
}


}

</style>

