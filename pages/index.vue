<template>
  <div class="carousel-wrapper">
    <client-only>
      <agile :options="options">
        <div v-for="i in 5" :key="i" class="img-wrapper">
          <img :src="`./${i}-200x100.jpg`" />
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
        navButtons: false,
        dots: false
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
</style>
