<template>
  <div class="section text-center" id="experiences">
    <hr />
    <div class="container">
      <h2 class="title">Experiences</h2>
      <div class="team">
        <div class="md-layout">
          <div 
            class="md-layout-item md-medium-size-50 md-small-size-100"
            v-for="company in companys" 
            :key="company.id"
          >
            <div class="team-player">
              <md-card class="md-card-plain">
                <div class="md-layout-item md-size-50 mx-auto">
                  <img
                    :src="company.image"
                    :alt="company.name"
                    class="img-fluid"
                  />
                </div>
                <h4 class="card-title">
                  {{company.name}}
                  <br />
                  <small class="card-description text-muted">
                    {{company.start_date}} - {{company.end_date}}
                  </small>
                </h4>
                <md-card-content>
                  <p class="card-description">
                    {{company.description}}
                  </p>
                </md-card-content>
                <md-card-actions class="text-center">
                  <md-button
                    v-if="company.skype"
                    :href="company.skype"
                    target="_blank"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-twitter"></i>
                  </md-button>
                  <md-button
                    v-if="company.instagram"
                    :href="company.instagram"
                    target="_blank"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-instagram"></i>
                  </md-button>
                  <md-button
                    v-if="company.facebook"
                    :href="company.facebook"
                    target="_blank"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-facebook-square"></i>
                  </md-button>
                  <md-button
                    v-if="company.linkedin"
                    :href="company.linkedin"
                    target="_blank"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-linkedin"></i>
                  </md-button>
                  <md-button
                    v-if="company.email"
                    :href="company.email"
                    target="_blank"
                    class="md-just-icon md-simple"
                  >
                    <i class="fas fa-envelope-square"></i>
                  </md-button>
                  <md-button
                    v-if="company.website"
                    :href="company.website"
                    target="_blank"
                    class="md-just-icon md-simple"
                  >
                    <i class="fas fa-external-link-square-alt"></i>
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
      let companys = [
        {
          id: "sonivy",
          image: require("@/assets/img/experiences/sonivy.png"),
          name: "Sonivy Technology Limited",
          website: "https://www.sonivy.com/",
          facebook: "https://www.facebook.com/SonivyTechnologyLimited/",
          linkedin: "https://www.linkedin.com/company/sonivy-technology-limited/",
          email: "info@sonivy.com",
          start_date: this.getDate(2017, 5, null),
          end_date: this.getDate(null, null, null),
          description: "You can write here details about one of your team members. You can give more details about what they do. You can write here details about one of your team members. You can give more details about what they do."
        },
        {
          id: "gti",
          image: require("@/assets/img/experiences/gti.png"),
          name: "GTI",
          website: "https://www.gti.com.hk/",
          facebook: "https://www.facebook.com/GTIhongkong/",
          linkedin: "https://www.linkedin.com/company/gti-ltd",
          email: "inquiry@gti.com.hk",
          start_date: this.getDate(2015, 7, null),
          end_date: this.getDate(2016, 8, null),
          description: "You can write here details about one of your team members. You can give more details about what they do. You can write here details about one of your team members. You can give more details about what they do."
        }
      ]

      return {
        companys
      }
    },
    methods: {
      getDate(year, month, day) {
        let date = new Date(year, month - 1, day);
        let dateStrParts = date.toString().split(" ");
        
        if(year && month && !day){
           return `${dateStrParts[1]}, ${dateStrParts[3]}`;
        }
        else if(year && month && day){
           return `${date.getDate()} ${dateStrParts[1]}, ${dateStrParts[3]}`;
        }else if(!year && !month && !day){
          return "Now"
        }
      }
    }
  }
</script>

<style lang="scss" scoped>
</style>
