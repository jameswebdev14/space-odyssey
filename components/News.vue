<template>
  <div id="news-feed">
    <h5 id="feed-section-title">NASA Latest Feed</h5>
    <h6 id="feed-title">{{ data.title }}</h6>
    <h6 id="feed-explanation">{{ data.explanation }}</h6>
    <a :href="data.url">{{ data.url }}</a>
  </div>
</template>

<script>
export default {
  name: "nasa",
  props: {
    nasa_data: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      data: this.nasa_data
    };
  },
  mounted() {
    console.log(this.data);
  }
};
</script>

<style scoped>
#news-feed {
  margin-bottom: 30px !important;
}

#feed-section-title {
  font-size: 1.2rem;
  margin-bottom: 20px;
  color: #c0c0c0;
  letter-spacing: 3px;
  text-shadow: 2px 0 red;
}

#feed-title {
  margin-bottom: 20px;
  font-size: 1rem;
  color: #c0c0c0;
  font-weight: bolder;
  letter-spacing: 3px;
}

/* MEDIUM UP VIEW */
@media screen and (min-width: 768px) {
  #feed-section-title {
    font-size: 1.7rem;
    margin-bottom: 30px;
    color: #c0c0c0;
    text-shadow: 2px 0 red;
  }

  #feed-title {
    margin-bottom: 30px;
    font-size: 1.4rem;
    color: #c0c0c0;
    font-weight: bolder;
    letter-spacing: 5px;
  }

  #feed-explanation {
    margin-bottom: 10px;
    font-size: 1.2rem;
    padding: 20px;
  }
}
</style>
