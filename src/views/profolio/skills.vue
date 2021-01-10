<template>
  <div>
    <hr>
    <h2 class="title text-center" id="skills">Skills</h2>
    <div class="text-center">Click the badge if you want ;)</div>
    <div class="section text-center">
      <div class="team">
        <div class="md-layout" id="major_skills">
          <div 
            class="md-layout-item md-xlarge-size-33 md-large-size-33 md-medium-size-33 md-small-size-50"
            v-for="skill in major_skills" 
            :key="skill.id"
          >
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="skill.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  {{skill.name}}
                  <br />
                  <small class="card-description text-muted">
                    {{skill.description}}
                  </small>
                </h4>
                <div
                  v-for="tag in skill.tags" 
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
        <div class="md-layout" id="minor_skills">
          <div 
            class="md-layout-item md-xlarge-size-20 md-large-size-20 md-medium-size-20 md-small-size-33"
            v-for="skill in minor_skills" 
            :key="skill.id"
          >
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="skill.image"
                    alt="Thumbnail Image"
                    class="img-raised img-fluid"
                  />
                </div>
                <h4 class="card-title"></h4>
                <div
                  @click="clicked_tag(skill)"
                  :class="selected_tag(skill)"
                >
                  {{skill.name}}
                </div>
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
      let major_skills = [
        { // nodejs
          id: "nodejs",
          image: require("@/assets/img/skills/nodejs.png"),
          name: "Nodejs",
          description: "Backend",
          tags: [
            { id: "node_i18n", name: "i18n", clicked: false },
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
            { id: "node_cron", name: "Cron Job", clicked: false },
            { id: "node_redis", name: "Redis", clicked: false }
          ]
        },
        { // aws
          id: "aws",
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
        },
        { // arduino
          id: "arduino",
          image: require("@/assets/img/skills/arduino.png"),
          name: "Arduino",
          description: "IoT",
          tags: [
            { id: "arduino_esp8266", name: "WIFI ESP8266", clicked: false },
            { id: "arduino_bigdata", name: "Big Data", clicked: false },
            { id: "arduino_robot", name: "Robot Car", clicked: false },
            { id: "arduino_home", name: "Home security", clicked: false },
            { id: "arduino_music", name: "Music Box", clicked: false },
          ] 
        },
        { // python
          id: "python",
          image: require("@/assets/img/skills/python.png"),
          name: "Python",
          description: "Backend",
          tags: [
            { id: "py_system", name: "System Control", clicked: false },
            { id: "py_curl", name: "curl", clicked: false },
            { id: "py_face", name: "Face Recognition", clicked: false },
            { id: "py_bigdata", name: "Big Data", clicked: false },
          ]
        },
        { // vue
          id: "vue",
          image: require("@/assets/img/skills/vue.png"),
          name: "Vue",
          description: "Frontend",
          tags: [
            { id: "vue_admin", name: "Admin Panel", clicked: false },
            { id: "vue_portfolio", name: "Portfolio", clicked: false },
            { id: "vue_cli_service", name: "vue-cli-service", clicked: false },
            { id: "vue_material", name: "Material", clicked: false },
            { id: "vue_i18n", name: "i18n", clicked: false }
          ] 
        },
        { // dotnet
          id: "dotnet",
          image: require("@/assets/img/skills/dotnet.png"),
          name: ".Net",
          description: "Agile Development",
          tags: [
            { id: "dotnet_i18n", name: "i18n", clicked: false },
            { id: "dotnet_iis", name: "IIS", clicked: false },
            { id: "dotnet_mssql", name: "MSSQL", clicked: false },
            { id: "dotnet_vb", name: "VB", clicked: false },
            { id: "dotnet_c", name: "C", clicked: false },
            { id: "dotnet_cshap", name: "C#", clicked: false },
            { id: "dotnet_erp", name: "ERP", clicked: false },
            { id: "dotnet_crm", name: "CRM", clicked: false },
          ] 
        }
      ]
      let minor_skills = [
        { // go
          id: "go",
          image: require("@/assets/img/skills/go.png"),
          name: "Go",
          clicked: false
        },
        { // expo
          id: "expo",
          image: require("@/assets/img/skills/expo.png"),
          name: "Expo",
          clicked: false
        },
        { //processing
          id: "processing",
          image: require("@/assets/img/skills/processing.png"),
          name: "Processing",
          clicked: false
        }
      ]
      return {
        major_skills,
        minor_skills
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
