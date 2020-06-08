<template>
  <div class="container">
    <button @click="moveUp()" class="up-btn">Up</button>
    <div class="social">
      <social-links />
    </div>
    <div class="copyright">
      © Copyright 2020
      <span class="title">Prashant</span>. All rights reserved.
      This page is built in<span class="title">Vue js</span>
    </div>
  </div>
</template>

<script>
import SocialLinks from "./Social-links.vue";
export default {
  name: "Footer",
  components: { SocialLinks },
  methods: {
    moveUp: function() {
      window.scrollTo({top: 0, behavior: 'smooth'});
    }
  }
};
</script>>
<style scoped>
.container {
  background: #3c3c39;
  width: 100%;
  position: relative;
  bottom: 0px;
  color: #ffffff;
  z-index: 12;
  padding-bottom: 20px;
}
.up-btn {
  border-radius: 50%;
  height: 45px;
  width: 45px;
  border: none;
  background: #1cb698;
  font-size: 16px;
  color: #ffffff;
  font-weight: bold;
  position: absolute;
  top: -20px;
  outline: none;
  cursor: pointer;
  transition: all 0.5s ease;
}
.title {
    color: #1cb698;
    font-weight: bold;
    padding: 0 5px;
}
.social {
  padding-top: 20px;
}
</style>