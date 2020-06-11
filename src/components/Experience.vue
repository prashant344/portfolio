<template>
  <div class="details-container">
    <div class="title-container">
      <span class="title">Education</span>
      <span class="title">Experience</span>
    </div>
    <div class="title-container-small-screen">
      <span class="title">Education</span>
    </div>
    <div class="edu-exp-details-container">
      <div class="edu-container fade-in-section education-details">
        <div class="edu-cards">
          <div class="card-main-content">KC College of Engineering & IT</div>
          <div class="card-content">Punjab Technical University</div>
          <div class="card-content">B.Tech</div>
          <div class="card-main-content">2010 - 2014</div>
        </div>
        <div class="edu-cards">
          <div class="card-main-content">R.P.S. Residential School</div>
          <div class="card-content">C.B.S.E.</div>
          <div class="card-content">12th</div>
          <div class="card-main-content">2008 - 2010</div>
        </div>
      </div>
      <div class="title-container-small-screen">
        <span class="title">Experience</span>
      </div>
      <div class="exp-container fade-in-section experience-details">
        <div class="exp-cards">
          <div class="card-main-content">CA Technologies (Broadcom)</div>
          <div class="card-content">Bangalore</div>
          <div class="card-content">Senior Software Engineer</div>
          <div class="card-main-content">Nov 2018 - June 2020</div>
        </div>
        <div class="exp-cards">
          <div class="card-main-content">Tesco</div>
          <div class="card-content">Bangalore</div>
          <div class="card-content">Software Enginner</div>
          <div class="card-main-content">Jan 2015 - Nov 2018</div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.edu-exp-details-container {
  display: flex;
}
.title-container, .title-container-small-screen{
  display: flex;
  justify-content: space-evenly;
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 20px !important;
}
.title-container span:hover, .title-container-small-screen span:hover {
  color: #1cb698;
  transition: all 0.5s ease;
}
.title-container-small-screen {
  display: none;
}
.edu-cards {
  width: 90%;
  max-width: 400px;
  padding: 30px;
  box-sizing: border-box;
  box-shadow: 0 0 25px rgba(68, 68, 68, 0.07);
  background: #fff;
  margin-bottom: 40px !important;
  text-align: left;
  border-right: 2px solid #1cb698;
  position: relative;
}
.edu-cards:before {
  content: "";
  display: inline-block;
  position: absolute;
  background-color: #1cb698;
  border-radius: 10px;
  width: 12px;
  height: 12px;
  top: 50%;
  right: -43px;
  border: 2px solid #1cb698;
  z-index: 2;
  transform: translateY(-45%);
}
.edu-cards:after {
  content: "";
  display: inline-block;
  position: absolute;
  background-color: #1cb698;
  border-radius: 10px;
  width: 36px;
  height: 2px;
  top: 50%;
  right: -37px;
  z-index: 1;
}
.exp-cards {
  max-width: 400px;
  width: 90%;
  padding: 30px;
  box-sizing: border-box;
  box-shadow: 0 0 25px rgba(68, 68, 68, 0.07);
  background: #fff;
  margin-bottom: 40px !important;
  text-align: left;
  border-left: 2px solid #1cb698;
  position: relative;
}
.exp-cards:before {
  content: "";
  display: inline-block;
  position: absolute;
  background-color: #1cb698;
  border-radius: 10px;
  width: 12px;
  height: 12px;
  top: 50%;
  left: -43px;
  border: 2px solid #1cb698;
  z-index: 2;
  transform: translateY(-45%);
}
.exp-cards:after {
  content: "";
  display: inline-block;
  position: absolute;
  background-color: #1cb698;
  border-radius: 10px;
  width: 36px;
  height: 2px;
  top: 50%;
  left: -37px;
  z-index: 1;
}
.details-container {
  padding-top: 30px !important;
  background: #f6f7fe;
  display: flex;
  padding-bottom: 100px;
  flex-direction: column;
}
.education-details {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  width: 50%;
  margin-right: 50px !important;
  border-right: 1px solid #a1a1a1;
  padding-right: 34px !important;
  height: 378px;
}
.experience-details {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  width: 50%;
  margin-left: 50px !important;
  border-left: 1px solid #a1a1a1;
  padding-left: 34px !important;
  height: 378px;
}
.card-main-content {
  font-size: 16px;
  font-weight: bold;
  padding-bottom: 10px;
  color: #1cb698;
}
.card-content {
  font-size: 16px;
  font-weight: bold;
}

@media screen and (max-width: 840px) {
  .edu-exp-details-container {
    flex-direction: column;
  }
  .education-details,
  .experience-details {
    width: 80%;
    height: auto;
    align-items: flex-start;
  }
  .education-details {
    margin-left: 50px !important;
    margin-right: 0px !important;
    border-left: 1px solid #a1a1a1;
    border-right: 0;
    padding-left: 34px !important;
  }
  .experience-details {
    margin-left: 0px;
  }
  .edu-cards {
    border-left: 2px solid #1cb698;
    border-right: none;
  }
  .edu-cards:after {
    left: -37px;
    right: 0;
  }
  .edu-cards:before {
    left: -43px;
    right: 0;
  }
  .title-container {
    display: none;
  }
  .title-container-small-screen {
    display: block;
  }
  .details-container {
    align-items: center;
    justify-content: center;
  }
}
</style>