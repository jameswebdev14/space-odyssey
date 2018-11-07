<template>
  <div id="news-feed">
    <h5 id="feed-section-title">NASA Latest Feed</h5>
    <h6 id="feed-title">{{ data.title }}</h6>
    <h6 id="feed-explanation">{{ data.explanation }}</h6>
    <a :href="data.url">Link</a>
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
  width: 100%;
  padding: 5px;
  margin-bottom: 30px;
  display: flex;
  flex-flow: column;
  background-color: rgba(0, 0, 0, 0.5);
}

#news-feed a {
  font-size: 0.8rem;
  justify-self: flex-start;
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
@media screen and (min-width: 991px) {
  #news-feed {
    padding: 0 20px 20px 20px;
  }

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
