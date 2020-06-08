<template>
  <div id="about" class="container fade-in-section">
    <div class="image-container">
      <img class="about-img" src="../assets/about.jpg" />
    </div>
    <div class="text-container">
      <h2>{{ about.title }}</h2>
      <div class="text">
        I am
        <span class="title">{{ about['sub-title'] }}</span>
      </div>
      <div>{{ about.experience }}</div>

      <div>{{ about.myself }}</div>
      <div class="text">{{ about['tech-exp'] }}</div>
      <div class="info">
        <span class="title">{{ about['name-label'] }}</span>
        <span>:</span>
        <span class="value">{{ about['sub-title']}}</span>
      </div>
      <div class="info">
        <span class="title">{{ about['phone-label'] }}</span>
        <span>:</span>
        <span class="value">{{ about['phone-value'] }}</span>
      </div>
      <div class="info">
        <span class="title">{{ about['email-label'] }}</span>
        <span>:</span>
        <span class="value">{{ about['email-value'] }}</span>
      </div>
      <div class="info">
        <span class="title">{{ about['address-label'] }}</span>
        <span>:</span>
        <span class="value">{{ about['address-value'] }}</span>
      </div>
      <a class="download-link" :href="`${publicPath}resume.pdf`" download>
        <button class="download-btn">{{ about['download-resume-label'] }}</button>
      </a>
    </div>
  </div>
</template>

<script>
import { about } from "../config/message";

export default {
  data: () => ({ publicPath: process.env.BASE_URL, about })
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  margin: 50px !important;
  justify-content: center;
}
.about-img {
  max-width: 300px;
  width: 90%;
  padding: 14px;
  background: #fff;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.25);
}
.text-container {
  display: flex;
  position: relative;
  flex-direction: column;
  text-align: left;
  margin-left: 70px !important;
}
.title {
  color: #1cb698;
  font-weight: bold;
  margin-right: 40px !important;
}
.value {
  margin-left: 20px !important;
}
.info {
  margin-top: 10px !important;
}
.download-link {
  width: 160px;
}
.text {
  margin: 10px 0 !important;
}
.download-btn {
  width: 160px;
  height: 40px;
  background: #1cb698;
  color: #ffffff;
  border: 0;
  cursor: pointer;
  outline: none;
  border-radius: 5px;
  font-size: 14px;
  margin-top: 20px !important;
}
p {
  padding: 20px 0;
}
.image-container {
  display: inline-block;
  background-color: #ffffff;
  position: relative;
  max-width: 328px;
  height: 50%;
}
.image-container::after {
  background: #969696;
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  z-index: -10;
  transform: rotate(-6deg);
  -moz-transform: rotate(-6deg);
  -ms-transform: rotate(-6deg);
  -o-transform: rotate(-6deg);
  -moz-box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.25);
  -webkit-box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.25);
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.25);
}

@media screen and (max-width: 840px) {
  .container {
    flex-direction: column;
    align-items: center;
  }
  .image-container {
    margin-bottom: 60px !important;
  }
  .text-container {
    margin-left: 0px;
    margin: 0 auto !important;
  }
}
</style>