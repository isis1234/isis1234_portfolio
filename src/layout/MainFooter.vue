<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <nav>
        <ul>
          <li>
            <a href="#/basic_elements">
              Basic Element
            </a>
          </li>
          <li>
            <a href="#/landing">
              Landing
            </a>
          </li>
          <li>
            <a 
              href="https://demos.creative-tim.com/vue-material-kit/documentation/"
              target="_blank">
              Documentation
            </a>
          </li>
          <li>
            <a 
              href="https://materialdesignicons.com/"
              target="_blank">
              icons
            </a>
          </li>
        </ul>
      </nav>
      <div class="copyright">
        &copy; {{ year }}, made with by
        Tang Wing Yu<md-icon>favorite</md-icon>.
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style></style>
