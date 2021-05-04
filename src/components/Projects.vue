<template>
  <div id="projects" class="projects">
    <div class="container-title">PROJECTS</div>
    <div class="project-container fade-in-section">
      <div class="project-card fade-in-section">
        <img class="banner" src="../assets/clubcard.jpg" />
        <div class="title">{{ projects['tesco'].title }}</div>
        <div class="time-period">Tesco (Jan 2015 - Nov 2018)</div>
        <div class="desc">
          <div class="sub-title">About</div>
          <div>{{ projects['tesco'].about }}</div>
          <div class="sub-title">Technologies Used</div>
          <div>{{ projects['tesco'].tech }}</div>
        </div>
        <button class="read-more" @click="showDetails('tesco')">Read more</button>
      </div>
      <div class="project-card fade-in-section">
        <img class="banner" src="../assets/analytics.jpg" />
        <div class="title">Analytics for API Management</div>
        <div class="time-period">Broadcom (Nov 2018 - Jun 2020)</div>
        <div class="desc">
          <div class="sub-title">About</div>
          <div>
            This project is mainly a website which shows Analytics data in the form of trend charts and graphs.
            Each graph shows the analytical data like API hits, API latency and API Errors in the form of trend charts.
          </div>
          <div class="sub-title">Technologies Used</div>
          <div>React Js, Javascript, Java, Druid, Docker, HTML 5, Victory Js, CSS3</div>
        </div>
        <button class="read-more" @click="showDetails('ca')">Read more</button>
      </div>
      <div class="project-details" v-show="!isHidden">
        <div class="detail-sub-title">{{ getCardDetails().title }}</div>
        <div class="details-about">
          <div class="detail-sub-title">About</div>
          {{ getCardDetails().about }}
        </div>
        <div class="details-role">
          <div class="detail-sub-title">Roles & Responsibilities</div>
          <ul>
            <li v-for="(role,index) in getCardDetails().roles" :key="index">{{ role }}</li>
          </ul>
        </div>
        <div class="details-tech">
          <div class="detail-sub-title">Technologies Used</div>
          <div>{{ getCardDetails().tech }}</div>
        </div>
      </div>
      <div class="overlay" @click="isHidden = true" v-show="!isHidden" />
    </div>
  </div>
</template>

<script>
export default {
  el: "#projects",
  data() {
    return {
      isHidden: true,
      selectedCard: "tesco",
      projects: {
        tesco: {
          title: "Tesco Clubcard",
          about:
            "Tesco has a website for the customers having clubcard where customers can view the products and place an order for the product. This website has complete set of pages right from listing of products to the order placement and order confirmation.",
          roles: [
            "Worked on creating components in React Js for the website from scratch and integrating the components with the backend data exposed by Web API services using GraphQL and Apollo Js",
            "Developed website navigation for Desktop and for Mobile, and pages like product details page, product listing page, basket page and other pages using React Js and made it responsive using SASS and CSS media queries.",
            "Developed GraphQL endpoint to hit webapi services exposed to internet.",
            "Developed Common reusable components in React Js which can be used in other React components.",
            "Developed the application for responsive to different screen resolutions using SASS and CSS media queries for all the viewports.",
            "Used multiple JS libraries like Chai, Mocha, Jest and Enzyme to write unit test cases for the components."
          ],
          tech: "React Js, Javascript, Web API, GraphQL, HTML 5, CSS3, SASS"
        },
        ca: {
          title: "Analytics for API Management",
          about:
            "This project is mainly a website which shows Analytics data in the form of trend charts and graphs. It consisted of multiple Reports where each report has multiple charts or graphs. Each graph shows the analytical data like API hits, API latency and API Errors in the form of trend charts. Each graph can be filtered by using various filter types and date ranges.",
          roles: [
            "Worked as a frontend developer and built Analytics pages from scratch using React Js and Redux Js",
            "Created multiple charts using Victory js in React for Analytics webpages and support filtering options for the chart in order to get more drilled down data from the chart.",
            "Used Apis to integrate and support Real time Analytics solution.",
            "Developed Common reusable components in React Js which can be used in other React components.",
            "Worked on enabling an option and transforming a page that can be exported as a PDF.",
            "Used multiple JS libraries like Chai, Mocha, Jest and Enzyme to write unit test cases for the components."
          ],
          tech:
            "React Js, Javascript, Java, Druid, Docker, HTML 5, Victory Js, CSS3"
        }
      }
    };
  },
  methods: {
    getCardDetails: function() {
      return this.projects[this.selectedCard];
    },
    showDetails: function(name) {
      this.selectedCard = name;
      this.isHidden = false;
    }
  }
};
</script>
<style scoped>
.projects {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding-top: 40px;
}
.container-title {
  padding-bottom: 20px !important;
  font-size: 24px;
  font-weight: bold;
}
.project-container {
  background-image: url("../assets/projects.jpeg");
  background-attachment: fixed;
  width: 100%;
  padding: 20px;
  box-sizing: border-box;
  background-size: cover;
  background-position: center;
  display: flex;
  align-items: center;
  justify-content: center;
}
.project-card {
  height: 500px;
  background: #fff;
  border-radius: 5px;
  margin: 20px !important;
  position: relative;
  max-width: 500px;
}
.banner {
  width: 100%;
  height: 40%;
  object-fit: cover;
}
.title {
  font-weight: bold;
  font-size: 20px;
  text-align: left;
  padding: 10px 10px 0 10px;
  color: #1cb698;
}
.time-period {
  text-align: left;
  padding-left: 10px;
  font-size: 12px;
  color: #1cb698;
}
.desc {
  text-align: left;
  padding-left: 10px;
  padding-right: 10px;
  font-size: 14px;
}
.sub-title {
  padding: 10px 0;
  font-weight: bold;
}
.detail-sub-title {
  padding: 10px 0;
  font-weight: bold;
  color: #1cb698;
}
.read-more {
  height: 36px;
  width: 110px;
  background: #1cb698;
  color: #fff;
  font-size: 12px;
  font-weight: bold;
  border: none;
  margin-top: 22px !important;
  border-radius: 20px;
  float: right;
  margin-right: 10px !important;
  outline: none;
  position: absolute;
  bottom: 20px;
  cursor: pointer;
  right: 20px;
}
.project-details {
  position: absolute;
  max-width: 500px;
  margin: 0px auto !important;
  z-index: 1;
  background: #fff;
  border-radius: 5px;
  text-align: left;
  padding: 20px 20px 30px 20px;
  transition: all 0.5s ease;
}
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

@media screen and (max-width: 840px) {
  .project-container {
    flex-direction: column;
    background-attachment: unset;
  }
  .project-card {
    height: auto;
  }
  .read-more {
    position: relative;
  }
}
</style>