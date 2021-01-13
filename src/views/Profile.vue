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
                    id="icon"
                    :src="img"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <div class="name" id="info">
                  <h3 class="title">Tang Wing Yu</h3>
                  <h6>Software Developer | Speaker</h6>
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
                    @click="qr_modal = true"
                    class="md-success md-normal md-round"
                  >
                    Website QR Code
                  </md-button>
                  <modal v-if="qr_modal" @close="qr_modal = false">
                    <template slot="header">
                      <h4 class="modal-title"><b></b></h4>
                    </template>
                    <template slot="body">
                      <img :src="qd_link" id="qr_link" />
                    </template>
                  </modal>
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p>
              Hi I'm Yu🤗 A Hong Konger and loving to work on mini one man
              project. This is my porfolio for present my mini-project only, you
              can contact me if you wanna know more in my project. I'm looking
              for any mini-workshop to share my skill and talk to any personal,
              feel free to contact me😊.
            </p>
          </div>
          <div class="profile-tabs">
            <Projects />
            <Skills />
            <Educations />
            <Experiences />
            <br />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Modal } from "@/components";
import { Skills, Experiences, Educations, Projects } from "./profolio";
export default {
  components: {
    Skills,
    Experiences,
    Educations,
    Projects,
    Modal
  },
  bodyClass: "profile-page",
  data() {
    return {
      qr_modal: false,
      qd_link: require("@/assets/img/portfolio.png")
    };
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/city-profile.jpg")
    },
    img: {
      type: String,
      default: require("@/assets/img/self.jpg")
      // default: require("@/assets/img/faces/christian.jpg")
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

#qr_link {
  transform: translate3d(0, 0, 0);
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
