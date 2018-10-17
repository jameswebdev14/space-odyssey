<template>
  <div class="container">
    <section id="universe">
      <section id="universe_text">
      <h5>
      
      
      
      </h5>
    </section>
      <div  id="images">
        <img src="../assets/img/solar.jpg" alt="Solar System" class="img-fluid">
        <img src="../assets/img/beyond_solar.jpg" alt="Solar System" class="img-fluid">
      </div>
    </section>
  </div>
</template>

<style scoped>
/* DEFAULT MOBILE VIEW */
#universe {
  display:flex;
  flex-flow: column;
  justify-content:center;
}

#universe_text {
  padding:5px;
}

#universe h5 {
  font-size:1rem;
}

#universe_img {
  display:flex;
  flex-wrap:wrap;
  justify-content: center;
  align-items:center;
  margin-bottom:20px;
}

img {
  max-width:700px;
}

/*  MEDIUM UP VIEW */
@media screen and (min-width:991px) {
#universe {
  flex-flow: row;
  justify-content:center;
  align-items: center;
}

#universe_text {
  margin: auto;
  padding:30px;
  font-size: 2rem;
}

#universe_img {
  display:flex;
  justify-content: space-evenly;
  margin-bottom:40px;
}

#universe_text h4 {
  font-size: 1.5rem;
  margin-bottom:20px;
}

#images img {
    max-width: 500px;
    margin-bottom:30px;
  }
}
