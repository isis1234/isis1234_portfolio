<template>
  <div>
    <hr>
    <h2 class="title text-center" id="skills">Skills</h2>
    <div class="section text-center">
      <div class="team">
        <div class="md-layout">
          <div id="nodejs" class="md-layout-item md-xlarge-size-30 md-large-size-30 md-medium-size-30 md-small-size-50">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="nodejs.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  {{nodejs.name}}
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
                  <badge type="default">Telegram Bot</badge>
                  <badge type="default">Axios</badge>
                  <badge type="default">Curl</badge>
                  <badge type="default">Cron Job</badge>
                </md-card-content>
              </md-card>
            </div>
          </div>
          <div id="aws" class="md-layout-item md-xlarge-size-30 md-large-size-30 md-medium-size-30 md-small-size-50">
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
                  {{aws.name}}
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
          <div id="arduino" class="md-layout-item md-xlarge-size-30 md-large-size-30 md-medium-size-30 md-small-size-50">
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
                  {{arduino.name}}
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
          <div id="python" class="md-layout-item md-xlarge-size-30 md-large-size-30 md-medium-size-30 md-small-size-50">
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
                  {{python.name}}
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
          <div id="vue" class="md-layout-item md-xlarge-size-30 md-large-size-30 medium-size-30 md-small-size-50">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="vue.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  {{vue.name}}
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
        </div>
        <div class="md-layout">
          <div id="go" class="md-layout-item md-xlarge-size-20 md-large-size-20 md-medium-size-20 md-small-size-33">
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
                  <badge type="default">{{go.name}}</badge>
                  <br />
                </h4>
              </md-card>
            </div>
          </div>
          <div id="expo" class="md-layout-item md-xlarge-size-20 md-large-size-20 md-medium-size-20 md-small-size-33">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="expo.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
                  />
                </div>
                
                <h4 class="card-title">
                  <badge type="default">{{expo.name}}</badge>
                  <br />
                </h4>
              </md-card>
            </div>
          </div>
          <div id="processing" class="md-layout-item md-xlarge-size-20 md-large-size-20 md-medium-size-20 md-small-size-33">
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="processing.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
                  />
                </div>
                
                <h4 class="card-title">
                  <badge type="default">{{processing.name}}</badge>
                  <br />
                </h4>
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
        vue: {
          image: require("@/assets/img/skills/vue.png"),
          name: "Vue"
        },
        nodejs: {
          image: require("@/assets/img/skills/nodejs.png"),
          name: "Nodejs"
        },
        aws: {
          image: require("@/assets/img/skills/aws.png"),
          name: "Amazon Web Services"
        },
        python: {
          image: require("@/assets/img/skills/python.png"),
          name: "Python"
        },
        arduino: {
          image: require("@/assets/img/skills/arduino.png"),
          name: "Arduino"
        },
        go: {
          image: require("@/assets/img/skills/go.png"),
          name: "Go"
        },
        expo: {
          image: require("@/assets/img/skills/expo.png"),
          name: "Expo"
        },
        processing: {
          image: require("@/assets/img/skills/processing.png"),
          name: "Processing"
        }
      }
    }
  };
</script>

<style lang="scss" scoped>
</style>
