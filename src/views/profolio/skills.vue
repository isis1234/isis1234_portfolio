<template>
  <div>
    <hr>
    <h2 class="title text-center" id="skills">Skills</h2>
    <div class="section text-center">
      <div class="team">
        <div class="md-layout">
          <div id="vue" class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="frontend.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  Vue.js
                  <br />
                  <small class="card-description text-muted">Frontend</small>
                </h4>

                <md-card-content>
                  <badge type="default">Admin Panel</badge>
                  <badge type="default">Portfolio</badge>
                  <badge type="default">vue-cli-service</badge>
                </md-card-content>
              </md-card>
            </div>
          </div>
          <div id="nodejs" class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="backend.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
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
                  <badge type="default">Admin Panel</badge>
                  <badge type="default">Socket I/O</badge>
                  <badge type="default">Express</badge>
                  <badge type="default">Fastify</badge>
                  <badge type="default">Firebase</badge>
                  <badge type="default">Blockchain</badge>
                  <badge type="default">ETH Contract</badge>
                  <badge type="default">Axios</badge>
                  <badge type="default">Curl</badge>
                  <badge type="default">Cron Job</badge>
                </md-card-content>
              </md-card>
            </div>
          </div>
          <div id="aws" class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="aws.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
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
                  <badge type="default">EC2</badge>
                  <badge type="default">S3</badge>
                  <badge type="default">DynamoDB</badge>
                  <badge type="default">RDS</badge>
                  <badge type="default">Lambda</badge>
                  <badge type="default">SNS</badge>
                  <badge type="default">IoT Core</badge>
                  <badge type="default">API Gateway</badge>
                  <badge type="default">IAM</badge>
                </md-card-content>
              </md-card>
            </div>
          </div>
        </div>
        <div class="md-layout">
          <div id="python" class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="python.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
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
                  <badge type="default">System Control Script</badge>
                  <badge type="default">Curl</badge>
                  <badge type="default">Face Recognition</badge>
                  <badge type="default">Big Data</badge>
                </md-card-content>
              </md-card>
            </div>
          </div>
          <div id="arduino" class="md-layout-item md-medium-size-33 md-small-size-100">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="arduino.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
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
                  <badge type="default">WiFi ESP8266</badge>
                  <badge type="default">Big Data IoT</badge>
                  <badge type="default">Robot Car</badge>
                  <badge type="default">Home Security</badge>
                  <badge type="default">Music Box</badge>
                </md-card-content>
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
                    class="img-raised img-fluid"
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
  import { Badge } from '@/components'
  export default {
    components: {
      Badge
    },
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
