<template>
  <div>
    <hr>
    <h2 class="title text-center" id="skills">Skills</h2>
    <div class="section text-center">
      <div class="team">
        <div class="md-layout">
          <div class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="frontend.image"
                    alt="Thumbnail Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  Vue.js
                  <br />
                  <small class="card-description text-muted">Frontend</small>
                </h4>

                <md-card-content>
                  <p class="card-description">
                    You can write here details about one of your team
                    members. You can give more details about what they do.
                    Feel free to add some <a href="#">links</a> for people
                    to be able to follow them outside the site.
                  </p>
                </md-card-content>

                <md-card-actions class="text-center">
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-twitter"></i>
                  </md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-instagram"></i>
                  </md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-facebook-square"></i>
                  </md-button>
                </md-card-actions>
              </md-card>
            </div>
          </div>
          <div class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="backend.image"
                    alt="Thumbnail Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  NodeJS
                  <br />
                  <small class="card-description text-muted"
                    >Backend</small
                  >
                </h4>

                <md-card-content>
                  <p class="card-description">
                    You can write here details about one of your team
                    members. You can give more details about what they do.
                    Feel free to add some <a href="#">links</a> for people
                    to be able to follow them outside the site.
                  </p>
                </md-card-content>

                <md-card-actions class="text-center">
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-twitter"></i>
                  </md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-linkedin"></i>
                  </md-button>
                </md-card-actions>
              </md-card>
            </div>
          </div>
          <div class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="aws.image"
                    alt="Thumbnail Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  AWS
                  <br />
                  <small class="card-description text-muted"
                    >Cloud Service</small
                  >
                </h4>

                <md-card-content>
                  <p class="card-description">
                    You can write here details about one of your team
                    members. You can give more details about what they do.
                    Feel free to add some <a href="#">links</a> for people
                    to be able to follow them outside the site.
                  </p>
                </md-card-content>

                <md-card-actions class="text-center">
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-twitter"></i>
                  </md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-linkedin"></i>
                  </md-button>
                </md-card-actions>
              </md-card>
            </div>
          </div>
        </div>
        <div class="md-layout">
          <div class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="python.image"
                    alt="Thumbnail Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  Python
                  <br />
                  <small class="card-description text-muted"
                    >Backend</small
                  >
                </h4>

                <md-card-content>
                  <p class="card-description">
                    You can write here details about one of your team
                    members. You can give more details about what they do.
                    Feel free to add some <a href="#">links</a> for people
                    to be able to follow them outside the site.
                  </p>
                </md-card-content>

                <md-card-actions class="text-center">
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-twitter"></i>
                  </md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-linkedin"></i>
                  </md-button>
                </md-card-actions>
              </md-card>
            </div>
          </div>
          <div class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="arduino.image"
                    alt="Thumbnail Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  Arduino
                  <br />
                  <small class="card-description text-muted"
                    >IOT</small
                  >
                </h4>

                <md-card-content>
                  <p class="card-description">
                    You can write here details about one of your team
                    members. You can give more details about what they do.
                    Feel free to add some <a href="#">links</a> for people
                    to be able to follow them outside the site.
                  </p>
                </md-card-content>

                <md-card-actions class="text-center">
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-twitter"></i>
                  </md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-linkedin"></i>
                  </md-button>
                </md-card-actions>
              </md-card>
            </div>
          </div>
          <div class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="go.image"
                    alt="Thumbnail Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  Go
                  <br />
                  <small class="card-description text-muted"
                    >Backend</small
                  >
                </h4>

                <md-card-content>
                  <p class="card-description">
                    You can write here details about one of your team
                    members. You can give more details about what they do.
                    Feel free to add some <a href="#">links</a> for people
                    to be able to follow them outside the site.
                  </p>
                </md-card-content>

                <md-card-actions class="text-center">
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-twitter"></i>
                  </md-button>
                  <md-button
                    href="javascript:void(0)"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-linkedin"></i>
                  </md-button>
                </md-card-actions>
              </md-card>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        frontend: {
          image: require("@/assets/img/skills/vue.png")
        },
        backend: {
          image: require("@/assets/img/skills/nodejs.png")
        },
        aws: {
          image: require("@/assets/img/skills/aws.png")
        },
        python: {
          image: require("@/assets/img/skills/python.png")
        },
        arduino: {
          image: require("@/assets/img/skills/arduino.png")
        },
        go: {
          image: require("@/assets/img/skills/go.png")
        }
      }
    }
  };
</script>

<style lang="scss" scoped>
</style>
