<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="headerStyle"
    ></parallax>
    <div class="main main-raised">
      <div class="section profile-content">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
                <div class="avatar">
                  <img
                    :src="img"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <div class="name">
                  <h3 class="title">Tang Wing Yu</h3>
                  <h6>Software Developer</h6>
                  <md-button
                    href="https://github.com/isis1234/isis1234_portfolio"
                    target="_blank"
                    class="md-just-icon md-simple"
                    >
                    <i class="fab fa-github"></i>
                  </md-button>
                  <md-button
                    href="https://www.linkedin.com/in/wing-yu-tang-127226120"
                    target="_blank"
                    class="md-just-icon md-simple"
                    >
                    <i class="fab fa-linkedin"></i>
                  </md-button>
                  <md-button
                    href="https://t.me/uuuuuzx"
                    target="_blank"
                    class="md-just-icon md-simple"
                    >
                      <i class="fab fa-telegram"></i>
                  </md-button>
                  <md-button 
                    target="_blank"
                    href="https://github.com/isis1234/isis1234_portfolio"
                    class="md-success md-normal md-round">
                    View My Resume
                  </md-button>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              An artist of considerable range, Chet Faker — the name taken by
              Melbourne-raised, Brooklyn-based Nick Murphy — writes, performs
              and records all of his own music, giving it a warm, intimate feel
              with a solid groove structure.
            </p>
          </div>
          <div class="profile-tabs">
            <Skills></Skills>
            <Experiences></Experiences>
            <Educations></Educations>
            <Projects></Projects>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Skills, Experiences, Educations, Projects } from "./profolio";
export default {
  components: {
    Skills, Experiences, Educations, Projects
  },
  bodyClass: "profile-page",
  data() {
    return {
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/city-profile.jpg")
    },
    img: {
      type: String,
      default: require("@/assets/img/faces/christian.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="scss" scoped>
  .section {
    padding: 0;
  }

  .profile-tabs::v-deep {
    .md-card-tabs .md-list {
      justify-content: center;
    }

    [class*="tab-pane-"] {
      margin-top: 3.213rem;
      padding-bottom: 50px;

      img {
        margin-bottom: 2.142rem;
      }
    }
  }

  .md-button i.fa-github {
    color: #000000 !important;
  }
  .md-button i.fa-linkedin {
    color: #0a66c2 !important;
  }
  .md-button i.fa-telegram {
    color: #1d98dc !important;
  }
</style>
