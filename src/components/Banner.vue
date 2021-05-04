<template>
  <div id="banner" class="banner">
    <div id="banner-overlay" class="banner-overlay" />
    <Profile />
  </div>
</template>
<script>
import Profile from "./Profile.vue";
export default {
  name: "Banner",
  components: {
    Profile
  }
};
</script>
<style>
.banner {
  background-image: url(../assets/banner-image.jpg);
  background-position: center;
  background-size: cover;
  position: relative;
  height: 100vh;
  background-attachment: fixed;
}
.banner-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}
@media screen and (max-width: 840px) {
  .banner {
    background-position: unset;
    background-attachment: unset;
  }
}
</style>