<template>
  <div id="app">
    <Banner />
    <Header />
    <About />
    <Skills />
    <Experience />
    <Projects />
    <Carousel />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Banner from "./components/Banner.vue";
import About from "./components/About.vue";
import Skills from "./components/Skills";
import Header from './components/header';
import Experience from './components/Experience';
import Footer from './components/Footer';
import Carousel from './components/Carousel';
import Projects from './components/Projects';
import Contact from './components/Contact';

export default {
  name: "App",
  components: {
    Banner,
    About,
    Skills,
    Header,
    Experience,
    Footer,
    Carousel,
    Projects,
    Contact,
  },
  mounted() {
    const myImgs = document.querySelectorAll(".fade-in-section");
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.intersectionRatio > 0) {
          entry.target.classList.add('isVisible');
        } else {
          entry.target.classList.remove('isVisible');
        }
      });
    });

    myImgs.forEach(image => {
      observer.observe(image);
    });
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  scroll-behavior: smooth;
  overflow-x: hidden;
}
.fade-in-section {
  opacity: 0;
  transform: translateY(20vh);
  visibility: hidden;
  transition: opacity 1s ease-out, transform 1.2s ease-out;
  will-change: opacity, visibility;
}
.fade-in-section.isVisible {
  opacity: 1;
  transform: none;
  visibility: visible;
}
</style>
