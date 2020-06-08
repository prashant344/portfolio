<template>
  <div class="header">
    <span class="header-item" @click="scrollToView('about')">About</span>
    <span class="header-item" @click="scrollToView('skills')">Skills</span>
    <span class="header-item" @click="scrollToView('projects')">Projects</span>
    <span class="header-item" @click="scrollToView('intrests')">Intrests</span>
    <span class="header-item" @click="scrollToView('contact')">Contact me</span>
  </div>
</template>

<script>
export default {
  methods: {
    scrollToView: function(id) {
      const elm = document.getElementById(id);
      elm.scrollIntoView({ block: "center" });
    }
  }
};
</script>
<style scoped>
.header {
  background-color: #39373a;
  width: 100%;
  display: flex;
  color: #fff;
  align-items: center;
  justify-content: flex-end;
  opacity: 0.75;
  position: sticky;
  top: 0;
  bottom: 0px;
  z-index: 11;
  height: 60px;
  box-shadow: 0px 3px 4.6px 0.3px rgba(0, 0, 0, 0.25);
}
.header-item {
  margin-right: 100px !important;
  font-weight: bold;
  border: 1px solid transparent;
  transition: all 0.7s ease;
  font-size: 18px;
}
.header-item:hover {
  border-bottom: 1px solid #1cb698;
  opacity: 1;
  color: #1cb698;
  cursor: pointer;
  transition: all 0.5s ease;
}
@media screen and (max-width: 840px) {
  .header {
    display: none;
  }
}
</style>