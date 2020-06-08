<template>
  <div id="intrests" class="carousel-container">
    <div class="title">MY INTRESTS</div>
    <div class="carousel fade-in-section">
      <button class="left-button" :class="{hidden: currentIndex === 1}" @click="prevSlide()">&lt;</button>
      <div class="card" :class="{active: currentIndex === 1}">
        <img src="../assets/travelling.jpg" />
        <span class="text">Travelling</span>
      </div>
      <div class="card" :class="{active: currentIndex === 2}">
        <img src="../assets/music.jpg" />
        <span class="text">Music</span>
      </div>
      <div class="card" :class="{active: currentIndex === 3}">
        <img src="../assets/cinema.jpg" />
        <span class="text">Movies</span>
      </div>
      <div class="card" :class="{active: currentIndex === 4}">
        <img src="../assets/coffee.jpg" />
        <span class="text">Coffee</span>
      </div>
      <button class="right-button" :class="{hidden: currentIndex === 4}" @click="nextSlide()">></button>
      <div class="overlay" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return { currentIndex: 1 };
  },
  mounted() {
    setInterval(() => {
      if (this.currentIndex === 4) {
        this.currentIndex = 0;
      }
      this.nextSlide();
    }, 5000);
  },
  methods: {
    nextSlide() {
      this.currentIndex++;
    },
    prevSlide() {
      this.currentIndex--;
    }
  }
};
</script>>
<style scoped>
.carousel-container {
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 24px;
  font-weight: bold;
  flex-direction: column;
  background: #f6f7fe;
  padding-top: 40px;
}
.title {
    margin-bottom: 10px!important;
}
.carousel {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 394px;
  position: relative;
  overflow: hidden;
  margin-bottom: 30px !important;
}
.card {
  width: 100%;
  position: absolute;
  opacity: 0;
  transition: all 1s ease;
}
.text {
  color: #ffffff;
  font-weight: bold;
  font-size: 50px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate3d(-50%, -50%, 0);
  z-index: 1;
  transition: all 0.5s ease;
  margin-left: 20px !important;
}
.text:hover {
  color: #1cb698;
  transition: all 0.5s ease;
}
.hidden {
  display: none;
}
img {
  height: 400px;
  width: 100%;
  object-fit: cover;
}
.card.active {
  opacity: 1;
  transition: all 1s ease;
}
button {
  position: absolute;
  height: 45px;
  z-index: 1;
  border: none;
  font-size: 26px;
  color: #1cb698;
  border-radius: 50%;
  background: #ffffff;
  width: 44px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 10px !important;
  cursor: pointer;
  outline: none;
  box-shadow: -1px 0px 8px 8px transparent;
  transition: all 0.5s ease;
}
button:hover {
  box-shadow: -1px 0px 8px 8px rgba(28, 182, 152, 1);
  transition: all 0.5s ease;
}
.right-button {
  right: 0;
}
.left-button {
  left: 0;
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.2);
}
</style>