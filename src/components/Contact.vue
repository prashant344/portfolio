<template>
  <div id="contact" class="contact-container">
    <div class="title">CONTACT ME</div>
    <div class="content fade-in-section">
      <div class="item fade-in-section">
        <font-awesome-icon :icon="['fas', 'envelope-open-text']" size="2x" />
        <span class="text">prashant.k.ranjan@gmail.com</span>
      </div>
      <div class="item fade-in-section">
        <font-awesome-icon :icon="['fas', 'phone-square']" size="2x" />
        <span class="text">9986901639</span>
      </div>
      <div class="item fade-in-section">
        <font-awesome-icon :icon="['fas', 'location-arrow']" size="2x" />
        <span class="text">Whitefield, Bangalore</span>
      </div>
    </div>
  </div>
</template>
<style scoped>
.contact-container {
  display: flex;
  background: #f6f7fe;
  flex-direction: column;
  padding-bottom: 30px !important;
}
.title {
  font-size: 24px;
  font-weight: bold;
}
.content {
  display: flex;
  justify-content: space-evenly;
  height: 200px;
  background: #ffffff;
  width: 90%;
  border-radius: 5px;
  align-items: center;
  margin: 20px auto !important;
  box-shadow: 0 0 30px #ededed;
}
.item {
  color: #1cb698;
  display: flex;
  align-items: center;
}
.text {
  padding-left: 10px;
}

@media screen and (max-width: 840px) {
  .content {
    flex-direction: column;
    align-items: flex-start;
    padding: 20px;
    box-sizing: border-box;
  }
}
</style>