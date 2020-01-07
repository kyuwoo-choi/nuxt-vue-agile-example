<template>
  <div class="carousel-wrapper">
    <client-only>
      <agile :options="options">
        <div v-for="i in 5" :key="i" class="img-wrapper">
          <img :src="`https://picsum.photos/200/100?random=${i}`" />
        </div>
      </agile>
    </client-only>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      options: {
        infinite: true,
        slidesToShow: 3,
        navButtons: false
      }
    }
  }
}
</script>

<style lang="scss">
.carousel-wrapper {
  padding: 40px;
  height: 180px;
}
.img-wrapper {
  text-align: center;
  img {
    margin: auto;
    width: 200px;
    height: 100px;
    background-image: linear-gradient(gray 100%, transparent 0);
  }
}
.agile__actions {
  margin: 10px;
}
.agile__dots {
  margin: auto;
  list-style: none;
  padding: 0;
  white-space: nowrap;
}
.agile__dot {
  margin: 0px 10px;
  button {
    background-color: #eee;
    border: none;
    border-radius: 50%;
    height: 10px;
    font-size: 0;
    line-height: 0;
    margin: 0;
    padding: 0;
    width: 10px;
  }
}
.agile__dot--current button {
  background-color: #888;
}
</style>
