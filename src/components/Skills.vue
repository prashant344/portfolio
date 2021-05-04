<template>
  <div id="skills" class="container fade-in-section">
    <div class="container-title">MY SKILLS</div>
    <div class="skills-container">
      <div class="skills-card fade-in-section">
        <img class="skills-logo" src="../assets/html5-logo.png" />
        <div class="overlay">
          <div class="overlay-inner">HTML 5</div>
        </div>
      </div>
      <div class="skills-card fade-in-section">
        <img class="skills-logo" src="../assets/css3-logo.png" />
        <div class="overlay">
          <div class="overlay-inner">CSS 3</div>
        </div>
      </div>
      <div class="skills-card fade-in-section">
        <img class="skills-logo" src="../assets/react-logo.png" />
        <div class="overlay">
          <div class="overlay-inner">React Js</div>
        </div>
      </div>
      <div class="skills-card fade-in-section">
        <img class="skills-logo" src="../assets/nodejs-logo.png" />
        <div class="overlay">
          <div class="overlay-inner">Node Js</div>
        </div>
      </div>
      <div class="skills-card fade-in-section">
        <img class="skills-logo" src="../assets/js-logo.png" />
        <div class="overlay">
          <div class="overlay-inner">Javascript</div>
        </div>
      </div>
      <div class="skills-card fade-in-section">
        <img class="skills-logo" src="../assets/graphql-logo.png" />
        <div class="overlay">
          <div class="overlay-inner">GraphQL</div>
        </div>
      </div>
      <div class="skills-card fade-in-section">
        <img class="skills-logo" src="../assets/vue-logo.png" />
        <div class="overlay">
          <div class="overlay-inner">Vue Js</div>
        </div>
      </div>
      <div class="skills-card fade-in-section">
        <img class="skills-logo" src="../assets/redux-logo.png" />
        <div class="overlay">
          <div class="overlay-inner">Redux Js</div>
        </div>
      </div>
      <div class="container-overlay" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Skills",
};
</script>

<style scoped>
.container {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}
.container-title {
  position: absolute;
  top: 0;
  margin-top: 72px !important;
  color: #fff;
  background: rgba(0, 0, 0, 0.4);
  margin: 0 auto;
  font-weight: bold;
  padding: 5px 25px;
  z-index: 11;
  font-size: 24px;
  border: 1px solid;
  transition: all 0.5s ease;
}
.container-title:hover {
  background: #1cb698;
  transition: all 0.5s ease;
}
.skills-logo {
  width: 100%;
  max-height: 165px;
}
.skills-container {
  display: flex;
  flex-direction: row;
  position: relative;
  padding: 110px 50px 50px 50px;
  width: 100%;
  margin-top: 30px !important;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  background-image: url("../assets/skills-image.jpg");
  background-size: cover;
  background-attachment: fixed;
}
.skills-card {
  padding: 20px;
  width: 150px;
  height: 145px;
  margin: 20px !important;
  z-index: 10;
  position: relative;
  background: #fff;
  opacity: 0.85;
}
.overlay:hover {
  opacity: 0.9;
}
.overlay:hover .overlay-inner {
  transform: translateY(0px);
}
.container-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  opacity: 0.4;
  background: rgba(0, 0, 0, 0.5);
}
.overlay {
  position: absolute;
  top: 0px;
  left: 0px;
  bottom: 0px;
  right: 0px;
  background: #1cb698;
  opacity: 0;
  -webkit-transition: all 0.5s ease;
  -moz-transition: all 0.5s ease;
  -ms-transition: all 0.5s ease;
  -o-transition: all 0.5s ease;
  transition: all 0.5s ease;
}
.overlay-inner {
  position: absolute;
  top: 35%;
  text-align: center;
  color: #fff;
  width: 100%;
  font-size: 30px;
  font-weight: bold;
  transition: all 0.5s;
  -webkit-transform: translateY(-30px);
  -moz-transform: translateY(-30px);
  -ms-transform: translateY(-30px);
  -o-transform: translateY(-30px);
  transform: translateY(-30px);
  text-transform: uppercase;
}
@media screen and (max-width: 840px) {
  .skills-container {
    background-attachment: unset;
  }
}
</style>>