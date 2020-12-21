<template>
  <div>
    <hr>
    <h2 class="title text-center" id="skills">Skills</h2>
    <div class="text-center">Feel free to select tags label ;)</div>
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
                    >{{nodejs.description}}</small
                  >
                </h4>
                <div
                  v-for="tag in nodejs.tags" 
                  :key="tag.id"
                  @click="clicked_tag(tag)"
                  :class="selected_tag(tag)"
                >
                  {{tag.name}}
                </div>
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
                    >{{aws.description}}</small
                  >
                </h4>
                <div
                  v-for="tag in aws.tags" 
                  :key="tag.id"
                  @click="clicked_tag(tag)"
                  :class="selected_tag(tag)"
                >
                  {{tag.name}}
                </div>
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
                    >{{arduino.description}}</small
                  >
                </h4>
                <div
                  v-for="tag in arduino.tags" 
                  :key="tag.id"
                  @click="clicked_tag(tag)"
                  :class="selected_tag(tag)"
                >
                  {{tag.name}}
                </div>
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
                    >{{python.description}}</small
                  >
                </h4>
                <div
                  v-for="tag in python.tags" 
                  :key="tag.id"
                  @click="clicked_tag(tag)"
                  :class="selected_tag(tag)"
                >
                  {{tag.name}}
                </div>
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
                  <small class="card-description text-muted">{{vue.description}}</small>
                </h4>
                <div
                  v-for="tag in vue.tags" 
                  :key="tag.id"
                  @click="clicked_tag(tag)"
                  :class="selected_tag(tag)"
                >
                  {{tag.name}}
                </div>
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
                  <div
                    @click="clicked_tag(go)"
                    :class="selected_tag(go)"
                  >
                    {{go.name}}
                  </div>
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
                  <div
                    @click="clicked_tag(expo)"
                    :class="selected_tag(expo)"
                  >
                    {{expo.name}}
                  </div>
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
                  <div
                    @click="clicked_tag(processing)"
                    :class="selected_tag(processing)"
                  >
                    {{processing.name}}
                  </div>
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
  export default {
    data() {
      let vue = {
        image: require("@/assets/img/skills/vue.png"),
        name: "Vue",
        description: "Frontend",
        tags: [
          { id: "vue_admin", name: "Admin Panel", clicked: false },
          { id: "vue_portfolio", name: "Portfolio", clicked: false },
          { id: "vue_cli_service", name: "vue-cli-service", clicked: false },
          { id: "vue_material", name: "Material", clicked: false }
        ] 
      }
      let nodejs = {
        image: require("@/assets/img/skills/nodejs.png"),
        name: "Nodejs",
        description: "Backend",
        tags: [
          { id: "node_admin", name: "Admin Panel", clicked: false },
          { id: "node_socket", name: "socket I/O", clicked: false },
          { id: "node_express", name: "Express", clicked: false },
          { id: "node_fastify", name: "Fastify", clicked: false },
          { id: "node_firebase", name: "Firebase", clicked: false },
          { id: "node_blockchain", name: "Blockchain", clicked: false },
          { id: "node_eth", name: "ETH contract", clicked: false },
          { id: "node_telegram", name: "Telegram Bot", clicked: false },
          { id: "node_axios", name: "axios", clicked: false },
          { id: "node_curl", name: "curl", clicked: false },
          { id: "node_cron", name: "Cron Job", clicked: false }
        ]
      }
      let aws = {
        image: require("@/assets/img/skills/aws.png"),
        name: "Amazon Web Services",
        description: "Cloud Services",
        tags: [ 
          { id:"aws_ec2", name: "EC2", clicked: false },
          { id:"aws_s3", name: "S3", clicked: false },
          { id:"aws_dynamodb", name: "DynamoDB", clicked: false },
          { id:"aws_rds", name: "RDS", clicked: false },
          { id:"aws_lambda", name: "Lambda", clicked: false },
          { id:"aws_sns", name: "SNS", clicked: false },
          { id:"aws_iot", name: "IoT Core", clicked: false },
          { id:"aws_apigateway", name: "API Gateway", clicked: false },
          { id:"aws_iam", name: "IAM", clicked: false }
        ]
      }
      let python = {
        image: require("@/assets/img/skills/python.png"),
        name: "Python",
        description: "Backend",
        tags: [
          { id: "py_system", name: "System Control", clicked: false },
          { id: "py_curl", name: "curl", clicked: false },
          { id: "py_face", name: "Face Recognition", clicked: false },
          { id: "py_bigdata", name: "Big Data", clicked: false },
        ]
      }
      let arduino = {
        image: require("@/assets/img/skills/arduino.png"),
        name: "Arduino",
        description: "IOT",
        tags: [
          { id: "arduino_esp8266", name: "WIFI ESP8266", clicked: false },
          { id: "arduino_bigdata", name: "Big Data", clicked: false },
          { id: "arduino_robot", name: "Robot Car", clicked: false },
          { id: "arduino_home", name: "Home security", clicked: false },
          { id: "arduino_music", name: "Music Box", clicked: false },
        ] 
      }
      let go = {
        image: require("@/assets/img/skills/go.png"),
        name: "Go",
        clicked: false
      }
      let expo = {
        image: require("@/assets/img/skills/expo.png"),
        name: "Expo",
        clicked: false
      }
      let processing = {
        image: require("@/assets/img/skills/processing.png"),
        name: "Processing",
        clicked: false
      }
      return {
        vue, nodejs, aws, python, arduino, go, expo, processing,
        major_skills: [ nodejs, aws, arduino, python, vue ],
        minor_skills: [ go, expo, processing ]
      }
    },
    methods: {
      selected_tag(tag){
        if(tag && tag.clicked)
          return "badge badge-success"
        else
          return "badge badge-default"
      },
      clicked_tag(tag){
        tag.clicked = !tag.clicked
      }
    }
  };
</script>

<style lang="scss" scoped>
</style>
