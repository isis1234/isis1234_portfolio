<template>
  <md-toolbar
    id="toolbar"
    md-elevation="0"
    class="md-transparent md-absolute"
    :class="extraNavClasses"
    :color-on-scroll="colorOnScroll"
  >
    <div class="md-toolbar-row md-collapse-lateral">
      <div class="md-toolbar-section-start">
        <h3 class="md-title">Tang Wing Yu</h3>
      </div>
      <div class="md-toolbar-section-end">
        <md-button
          class="md-just-icon md-simple md-toolbar-toggle"
          :class="{ toggled: toggledClass }"
          @click="toggleNavbarMobile()"
        >
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </md-button>

        <div class="md-collapse">
          <div class="md-collapse-wrapper">
            <mobile-menu nav-mobile-section-start="false" />
            <md-list>
              <md-list-item
                href="javascript:void(0)"
                @click="scrollToElement('info')"
              >
                <i class="material-icons">personal</i>
                <p>Info</p>
              </md-list-item>
              <md-list-item
                href="javascript:void(0)"
                @click="scrollToElement('skills')"
              >
                <i class="material-icons">content_paste</i>
                <p>Skills</p>
              </md-list-item>
              <md-list-item
                href="javascript:void(0)"
                v-if="showDownload"
                @click="scrollToElement('experiences')"
              >
                <i class="material-icons">work</i>
                <p>Experiences</p>
              </md-list-item>
              <md-list-item
                href="javascript:void(0)"
                @click="scrollToElement('educations')"
              >
                <i class="material-icons">school</i>
                <p>Educations</p>
              </md-list-item>
              <md-list-item
                href="javascript:void(0)"
                @click="scrollToElement('projects')"
              >
                <i class="material-icons">book</i>
                <p>Projects</p>
              </md-list-item>
              <hr />
              <md-list-item href="https://github.com/isis1234" target="_blank">
                <i class="fab fa-github"></i>
                <p class="hidden-lg">GitHub</p>
              </md-list-item>
              <md-list-item
                href="https://www.linkedin.com/in/wing-yu-tang-127226120"
                target="_blank"
              >
                <i class="fab fa-linkedin"></i>
                <p class="hidden-lg">LinkedIn</p>
              </md-list-item>
              <md-list-item href="https://t.me/uuuuuzx" target="_blank">
                <i class="fab fa-telegram"></i>
                <p class="hidden-lg">Telegram</p>
              </md-list-item>
              <md-list-item href="https://stackoverflow.com/users/19245388/yuu" target="_blank">
                <i class="fab fa-stack-overflow"></i>
                <p class="hidden-lg">Stack Overflow</p>
              </md-list-item>
            </md-list>
          </div>
        </div>
      </div>
    </div>
  </md-toolbar>
</template>

<script>
let resizeTimeout;
function resizeThrottler(actualResizeHandler) {
  // ignore resize events as long as an actualResizeHandler execution is in the queue
  if (!resizeTimeout) {
    resizeTimeout = setTimeout(() => {
      resizeTimeout = null;
      actualResizeHandler();

      // The actualResizeHandler will execute at a rate of 15fps
    }, 66);
  }
}

import MobileMenu from "@/layout/MobileMenu";
export default {
  components: {
    MobileMenu
  },
  props: {
    type: {
      type: String,
      default: "white",
      validator(value) {
        return [
          "white",
          "default",
          "primary",
          "danger",
          "success",
          "warning",
          "info"
        ].includes(value);
      }
    },
    colorOnScroll: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {
      extraNavClasses: "",
      toggledClass: false
    };
  },
  computed: {
    showDownload() {
      const excludedRoutes = ["login", "landing", "profile"];
      return excludedRoutes.every(r => r !== this.$route.name);
    }
  },
  methods: {
    bodyClick() {
      let bodyClick = document.getElementById("bodyClick");

      if (bodyClick === null) {
        let body = document.querySelector("body");
        let elem = document.createElement("div");
        elem.setAttribute("id", "bodyClick");
        body.appendChild(elem);

        let bodyClick = document.getElementById("bodyClick");
        bodyClick.addEventListener("click", this.toggleNavbarMobile);
      } else {
        bodyClick.remove();
      }
    },
    toggleNavbarMobile() {
      this.NavbarStore.showNavbar = !this.NavbarStore.showNavbar;
      this.toggledClass = !this.toggledClass;
      this.bodyClick();
    },
    handleScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      let navbarColor = document.getElementById("toolbar");
      this.currentScrollValue = scrollValue;
      if (this.colorOnScroll > 0 && scrollValue > this.colorOnScroll) {
        this.extraNavClasses = `md-${this.type}`;
        navbarColor.classList.remove("md-transparent");
      } else {
        if (this.extraNavClasses) {
          this.extraNavClasses = "";
          navbarColor.classList.add("md-transparent");
        }
      }
    },
    scrollListener() {
      resizeThrottler(this.handleScroll);
    },
    scrollToElement(element_id) {
      element_id = document.getElementById(element_id);
      // console.log(element_id)
      if (element_id) {
        element_id.scrollIntoView({ block: "center", behavior: "smooth" });
      }
    }
  },
  mounted() {
    document.addEventListener("scroll", this.scrollListener);
  },
  beforeDestroy() {
    document.removeEventListener("scroll", this.scrollListener);
  }
};
</script>
<!-- <style lang="scss" scoped>
  .md-collapse-lateral .md-collapse .md-list-item-content i.fa-github {
    color: #000000 !important;
  }
  .md-collapse-lateral .md-collapse .md-list-item-content i.fa-linkedin {
    color: #0a66c2 !important;
  }
  .md-collapse-lateral .md-collapse .md-list-item-content i.fa-telegram {
    color: #1d98dc !important;
  }
</style>
 -->
