<template>
  <div id="projects">
    <hr>
    <h2 class="title text-center">Projects</h2>
    <tabs
      :tab-name="['Software', 'Hardware', 'Speaker']"
      :tab-icon="['camera', 'palette', 'favorite']"
      plain
      nav-pills-icons
      color-button="success"
    >
      <template slot="tab-pane-1">
        <div class="md-layout">
          <div class="md-layout-item md-size-33 ml-auto">
            <div id="pj_self_porfolio">
              <img :src="self_porfolio.image[0]" class="rounded" @click="self_porfolio.modal=true"/>
              <modal v-if="self_porfolio.modal" @close="self_porfolio.modal=false" style="z-index: 1; position: absolute; ">
                <template slot="header">
                  <h4 class="modal-title"><b>{{self_porfolio.title}}</b></h4>
                </template>
                <template slot="body">
                  <md-card>
                    <carousel
                      :per-page="1"
                      loop
                      :speed="700"
                      autoplay
                      :autoplay-timeout="5000"
                      :mouse-drag="false"
                      navigationEnabled
                      navigationNextLabel="<i class='material-icons'>keyboard_arrow_right</i>"
                      navigationPrevLabel="<i class='material-icons'>keyboard_arrow_left</i>"
                    >
                      <slide><img :src="self_porfolio.image[0]" /></slide>
                      <!-- <slide><img :src="self_porfolio.image[1]" /></slide> -->
                    </carousel>
                   
                    <md-card-actions class="text-center">
                      <md-button
                        v-if="self_porfolio.github"
                        :href="self_porfolio.github"
                        target="_blank"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-github-square"></i>
                      </md-button>
                      <md-button
                        v-if="self_porfolio.demo"
                        :href="self_porfolio.demo"
                        target="_blank"
                        class="md-just-icon md-simple"
                      >
                        <i class="fas fa-external-link-square-alt"></i>
                      </md-button>
                    </md-card-actions>
                  </md-card>
                  <p>
                    {{self_porfolio.content}}
                  </p>
                  <div class="badge badge-success">{{self_porfolio.tag[0]}}</div>
                  <div class="badge badge-success">{{self_porfolio.tag[1]}}</div>
                  <md-card-actions class="text-center">
                    {{self_porfolio.project_date}} ({{self_porfolio.weeks}} weeks)
                  </md-card-actions>
                </template>
              </modal>
            </div>
            <div id="pj2">
              <img :src="pj2.image" class="rounded" @click="pj2.modal=true"/>
              <modal v-if="pj2.modal" @close="pj2.modal=false">
                <template slot="header">
                  <h4 class="modal-title"><b>PJ2</b></h4>
                </template>
                <template slot="body">
                  <md-button
                    class="md-simple md-just-icon md-round modal-default-button"
                    @click="pj2.modal=false"
                  >
                    <md-icon>clear</md-icon>
                  </md-button>
                  <p>pj2 Far far away.</p>
                </template>
              </modal>
            </div>
          </div>
          <div class="md-layout-item md-size-33 mr-auto">
            <div id="pj_yuyu_telegram_bot">
              <img :src="yuyu_telegram_bot.image[0]" class="rounded" @click="yuyu_telegram_bot.modal=true"/>
              <modal v-if="yuyu_telegram_bot.modal" @close="yuyu_telegram_bot.modal=false" style="z-index: 1; position: absolute; ">
                <template slot="header">
                  <h4 class="modal-title"><b>{{yuyu_telegram_bot.title}}</b></h4>
                </template>
                <template slot="body">
                  <md-card>
                    <carousel
                      :per-page="1"
                      loop
                      :speed="700"
                      autoplay
                      :autoplay-timeout="5000"
                      :mouse-drag="false"
                      navigationEnabled
                      navigationNextLabel="<i class='material-icons'>keyboard_arrow_right</i>"
                      navigationPrevLabel="<i class='material-icons'>keyboard_arrow_left</i>"
                    >
                      <slide><img :src="yuyu_telegram_bot.image[0]" /></slide>
                      <slide><img :src="yuyu_telegram_bot.image[1]" /></slide>
                      <slide><img :src="yuyu_telegram_bot.image[2]" /></slide>
                    </carousel>
                   
                    <md-card-actions class="text-center">
                      <md-button
                        v-if="yuyu_telegram_bot.github"
                        :href="yuyu_telegram_bot.github"
                        target="_blank"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-github-square"></i>
                      </md-button>
                      <md-button
                        v-if="yuyu_telegram_bot.demo"
                        :href="yuyu_telegram_bot.demo"
                        target="_blank"
                        class="md-just-icon md-simple"
                      >
                        <i class="fas fa-external-link-square-alt"></i>
                      </md-button>
                    </md-card-actions>
                  </md-card>
                  <p>
                    {{yuyu_telegram_bot.content}}
                  </p>
                  <div class="badge badge-success">{{yuyu_telegram_bot.tag[0]}}</div>
                  <div class="badge badge-success">{{yuyu_telegram_bot.tag[1]}}</div>
                  <md-card-actions class="text-center">
                    {{yuyu_telegram_bot.project_date}} ({{yuyu_telegram_bot.weeks}} weeks)
                  </md-card-actions>
                </template>
              </modal>
            </div>
            <div id="pj5">
              <img :src="pj5.image" class="rounded" @click="pj5.modal=true"/>
              <modal v-if="pj5.modal" @close="pj5.modal=false">
                <template slot="header">
                  <h4 class="modal-title"><b>PJ5</b></h4>
                  <md-button
                    class="md-simple md-just-icon md-round modal-default-button"
                    @click="pj5.modal=false"
                  >
                    <md-icon>clear</md-icon>
                  </md-button>
                </template>
                <template slot="body">
                  <p>pj5 Far far away.</p>
                </template>
              </modal>
            </div>
          </div>
          <div class="md-layout-item md-size-33 mr-auto">
            <div id="pj_MSDisplayAdapter_E6">
              <img :src="MSDisplayAdapter_E6.image[0]" class="rounded" @click="MSDisplayAdapter_E6.modal=true"/>
              <modal v-if="MSDisplayAdapter_E6.modal" @close="MSDisplayAdapter_E6.modal=false" style="z-index: 1; position: absolute; ">
                <template slot="header">
                  <h4 class="modal-title"><b>{{MSDisplayAdapter_E6.title}}</b></h4>
                </template>
                <template slot="body">
                  <md-card>
                    <carousel
                      :per-page="1"
                      loop
                      :speed="700"
                      autoplay
                      :autoplay-timeout="5000"
                      :mouse-drag="false"
                      navigationEnabled
                      navigationNextLabel="<i class='material-icons'>keyboard_arrow_right</i>"
                      navigationPrevLabel="<i class='material-icons'>keyboard_arrow_left</i>"
                    >
                      <slide><img :src="MSDisplayAdapter_E6.image[0]" /></slide>
                      <!-- <slide><img :src="self_porfolio.image[1]" /></slide> -->
                    </carousel>
                   
                    <md-card-actions class="text-center">
                      <md-button
                        v-if="MSDisplayAdapter_E6.github"
                        :href="MSDisplayAdapter_E6.github"
                        target="_blank"
                        class="md-just-icon md-simple"
                      >
                        <i class="fab fa-github-square"></i>
                      </md-button>
                      <md-button
                        v-if="MSDisplayAdapter_E6.demo"
                        :href="MSDisplayAdapter_E6.demo"
                        target="_blank"
                        class="md-just-icon md-simple"
                      >
                        <i class="fas fa-external-link-square-alt"></i>
                      </md-button>
                    </md-card-actions>
                  </md-card>
                  <p>
                    {{MSDisplayAdapter_E6.content}}
                  </p>
                  <div class="badge badge-success">{{MSDisplayAdapter_E6.tag[0]}}</div>
                  <div class="badge badge-success">{{MSDisplayAdapter_E6.tag[1]}}</div>
                  <md-card-actions class="text-center">
                    {{MSDisplayAdapter_E6.project_date}} ({{MSDisplayAdapter_E6.weeks}} weeks)
                  </md-card-actions>
                </template>
              </modal>
            </div>
          </div>
        </div>
      </template>

      <template slot="tab-pane-2">
        <div class="md-layout">
          <div class="md-layout-item md-size-25 ml-auto">
            <img :src="tabPane2[0].image" class="rounded" />
            <img :src="tabPane2[1].image" class="rounded" />
            <img :src="tabPane2[2].image" class="rounded" />
          </div>
          <div class="md-layout-item md-size-25 mr-auto">
            <img :src="tabPane2[3].image" class="rounded" />
            <img :src="tabPane2[4].image" class="rounded" />
          </div>
        </div>
      </template>

      <template slot="tab-pane-3">
        <div class="md-layout">
          <div class="md-layout-item md-size-25 ml-auto">
            <img :src="tabPane3[0].image" class="rounded" />
            <img :src="tabPane3[1].image" class="rounded" />
          </div>
          <div class="md-layout-item md-size-25 mr-auto">
            <img :src="tabPane3[2].image" class="rounded" />
            <img :src="tabPane3[3].image" class="rounded" />
            <img :src="tabPane3[4].image" class="rounded" />
          </div>
        </div>
      </template>
    </tabs>   
  </div>
</template>

<script>
import { Tabs, Modal } from "@/components";
export default {
  components: {
    Tabs, Modal,
  },
  data() {
    let software = [
      {
        id: "pj_self_porfolio",
        title: "Self Porfolio",
        modal: false,
        content: "My first portfolio which using vue template😃.",
        image: [
          require("@/assets/img/project_items/SelfPortfolio/1.png"),
          require("@/assets/img/examples/olu-eletu.jpg")
        ],
        tag: [ "Vue", "MATERIAL" ],
        project_date: this.getDate(2020, 12, null),
        weeks: 2,
        github: "https://github.com/isis1234/isis1234_portfolio",
        demo: "https://isis1234.github.io/isis1234_portfolio/"
      },
      {
        id: "pj_yuyu_telegram_bot",
        title: "Yu Telegram Bot",
        modal: false,
        content: "A reservation bot for remind you have a sit in the restaurant.",
        image: [
          require("@/assets/img/project_items/YuyuTelegramBot/1.png"),
          require("@/assets/img/project_items/YuyuTelegramBot/2.png"),
          require("@/assets/img/project_items/YuyuTelegramBot/3.png"),
        ],
        tag: [ "NodeJS", "Telegram Bot" ],
        project_date: this.getDate(2020, 10, null),
        weeks: 2,
        github: "https://github.com/isis1234/yuyu_telegram_bot",
        demo: "https://telegram.me/yuyu_test_bot"
      },
      {
        id: "pj_MSDisplayAdapterE6",
        title: "MSDisplayAdapter_E6",
        modal: false,
        content: "A script that auto start wireless projecter when i turnon my laptop.",
        image: [
          require("@/assets/img/project_items/MSDisplayAdapter_E6/1.gif"),
        ],
        tag: [ "Python", "Bat" ],
        project_date: this.getDate(2019, 12, null),
        weeks: 2,
        github: "https://github.com/isis1234/MSDisplayAdapter_E6",
      }
    ]
    return {
      self_porfolio: software[0],
      yuyu_telegram_bot: software[1],
      MSDisplayAdapter_E6: software[2],
      pj2: {
        image: require("@/assets/img/examples/studio-5.jpg"),
        modal: false,
      },
      pj5: {
        image: require("@/assets/img/examples/olu-eletu.jpg"),
        modal: false,
      },
      tabPane2: [
        { image: require("@/assets/img/examples/olu-eletu.jpg") },
        { image: require("@/assets/img/examples/clem-onojeghuo.jpg") },
        { image: require("@/assets/img/examples/cynthia-del-rio.jpg") },
        { image: require("@/assets/img/examples/mariya-georgieva.jpg") },
        { image: require("@/assets/img/examples/clem-onojegaw.jpg") }
      ],
      tabPane3: [
        { image: require("@/assets/img/examples/mariya-georgieva.jpg") },
        { image: require("@/assets/img/examples/studio-3.jpg") },
        { image: require("@/assets/img/examples/clem-onojeghuo.jpg") },
        { image: require("@/assets/img/examples/olu-eletu.jpg") },
        { image: require("@/assets/img/examples/studio-1.jpg") }
      ],
      carousel1: require("@/assets/img/nature-2.jpg"),
      carousel2: require("@/assets/img/nature.jpg"),
      carousel3: require("@/assets/img/nature-3.jpg")
    };
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
