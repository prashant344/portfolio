<template>
  <div class="profile-logo">
    <div class="ripple" />
    <img class="profile-pic" src="../assets/profile-pic.jpg" />
    <div class="intro-container">
      <h3 class="intro-name">I'm Prashant</h3>
      <div class="intro-about">
        <div class="intro-about-text" :style="style">{{text}}</div>
      </div>
    </div>
    <div class="social"><SocialLinks /></div>
  </div>
</template>

<script>
import SocialLinks from "./Social-links.vue";

export default {
  components: { SocialLinks },
  data() {
    return {
      style: {
        "max-width": "0%"
      },
      text: "Software Engineer"
    };
  },
  created() {
    var count = 0;
    var changeTextCounter = 0;
    var up = true;
    setInterval(() => {
      if (count == 0) {
        changeTextCounter += 1;
        if (changeTextCounter > 3) {
          changeTextCounter = 1;
        }
        changeText(changeTextCounter);
      }
      if (count == 0 || up) {
        count += 5;
      }
      if (count == 90) {
        up = false;
      }
      if (!up) {
        count -= 5;
        if (count == 0) {
          up = true;
        }
      }
      this.style["max-width"] = `${count}%`;
    }, 70);

    const changeText = changeTextCounter => {
      switch (changeTextCounter) {
        case 1:
          this.text = "Software Engineer";
          break;
        case 2:
          this.text = "Web Developer";
          break;
        case 3:
          this.text = "Frontend Expert";
          break;
        default:
          this.text = "Software Engineer";
      }
    };
  }
};
</script>

<style scoped>
img {
  border-radius: 50%;
  width: 200px;
  border: 12px solid #1cb698;
  z-index: 10;
}
.social {
  position: absolute;
  top: 85%;
}
.intro-container {
  position: absolute;
  top: 70%;
  color: #fafafa;
}
.intro-name {
  font-size: 34px;
  padding: 10px;
}
.intro-about-text::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 2px;
  height: 100%;
  background-color: #ffffff;
}
.intro-about-text {
  white-space: nowrap;
  overflow: hidden;
  max-width: 0%;
  margin-left: 15% !important;
  position: absolute;
  opacity: 1;
  font-size: 20px;
  padding-right: 5px;
  transition: all 70ms ease;
}
.hidden {
  opacity: 0;
}
.profile-logo {
  display: flex;
  align-items: center;
  justify-content: center;
  height: inherit;
}
@keyframes ripple {
  0% {
    box-shadow: 0 0 0 0 rgba(28, 182, 152, 0.2),
      0 0 0 1em rgba(28, 182, 152, 0.2), 0 0 0 3em rgba(28, 182, 152, 0.2),
      0 0 0 5em rgba(28, 182, 152, 0.2);
  }
  100% {
    box-shadow: 0 0 0 1em rgba(28, 182, 152, 0.2),
      0 0 0 3em rgba(28, 182, 152, 0.2), 0 0 0 5em rgba(28, 182, 152, 0.2),
      0 0 0 8em rgba(28, 182, 152, 0);
  }
}

.ripple {
  animation: ripple 1s linear infinite;
  animation-delay: 1s;
  content: "";
  border-radius: 50%;
  background-color: #fff;
  width: 150px;
  height: 150px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>