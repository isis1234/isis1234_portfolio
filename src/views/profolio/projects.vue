<template>
  <div id="projects">
    <hr />
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
          <div
            v-for="pj in software"
            class="md-layout-item md-size-33 ml-auto"
            :key="pj.id"
          >
            <img :src="pj.image[0]" class="rounded" @click="pj.modal = true" />
            <modal
              v-if="pj.modal"
              @close="pj.modal = false"
              style="z-index:2; position:absolute;"
            >
              <template slot="header">
                <h4 class="modal-title">
                  <b>{{ pj.title }}</b>
                </h4>
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
                    <slide
                      v-for="(image, index) in pj.image"
                      :key="`${pj.id}_image_${index}`"
                    >
                      <img :src="image" />
                    </slide>
                  </carousel>
                  <md-card-actions class="text-center">
                    <md-button
                      v-if="pj.github"
                      :href="pj.github"
                      target="_blank"
                      class="md-just-icon md-simple"
                    >
                      <i class="fab fa-github-square" />
                    </md-button>
                    <md-button
                      v-if="pj.demo"
                      :href="pj.demo"
                      target="_blank"
                      class="md-just-icon md-simple"
                    >
                      <i class="fas fa-external-link-square-alt" />
                    </md-button>
                  </md-card-actions>
                </md-card>
                <p>{{ pj.content }}</p>
                <div
                  v-for="(tag, index) in pj.tag"
                  :key="`${pj.id}_tag_${index}`"
                  class="badge badge-success"
                >
                  {{ tag }}
                </div>
                <md-card-actions class="text-center">
                  {{ pj.project_date }} ({{ pj.weeks }} weeks)
                </md-card-actions>
              </template>
            </modal>
          </div>
        </div>
      </template>

      <template slot="tab-pane-2">
        <div class="md-layout">
          <div
            v-for="pj in hardware"
            class="md-layout-item md-size-33 ml-auto"
            :key="pj.id"
          >
            <img :src="pj.image[0]" class="rounded" @click="pj.modal = true" />
            <modal
              v-if="pj.modal"
              @close="pj.modal = false"
              style="z-index:2; position:absolute;"
            >
              <template slot="header">
                <h4 class="modal-title">
                  <b>{{ pj.title }}</b>
                </h4>
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
                    <slide
                      v-for="(image, index) in pj.image"
                      :key="`${pj.id}_image_${index}`"
                    >
                      <img :src="image" />
                    </slide>
                  </carousel>
                  <md-card-actions class="text-center">
                    <md-button
                      v-if="pj.github"
                      :href="pj.guthub"
                      target="_blank"
                      class="md-just-icon md-simple"
                    >
                      <i class="fab fa-github-square" />
                    </md-button>
                    <md-button
                      v-if="pj.demo"
                      :href="pj.demo"
                      target="_blank"
                      class="md-just-icon md-simple"
                    >
                      <i class="fas fa-external-link-square-alt" />
                    </md-button>
                  </md-card-actions>
                </md-card>
                <p>{{ pj.content }}</p>
                <div
                  v-for="(tag, index) in pj.tag"
                  :key="`${pj.id}_tag_${index}`"
                  class="badge badge-success"
                >
                  {{ tag }}
                </div>
                <md-card-actions class="text-center">
                  {{ pj.project_date }} ({{ pj.weeks }} weeks)
                </md-card-actions>
              </template>
            </modal>
          </div>
        </div>
      </template>

      <template slot="tab-pane-3">
        <div class="md-layout">
          <div
            v-for="pj in speaker"
            class="md-layout-item md-size-33 ml-auto"
            :key="pj.id"
          >
            <img :src="pj.image[0]" class="rounded" @click="pj.modal = true" />
            <modal
              v-if="pj.modal"
              @close="pj.modal = false"
              style="z-index:2; position:absolute;"
            >
              <template slot="header">
                <h4 class="modal-title">
                  <b>{{ pj.title }}</b>
                </h4>
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
                    <slide
                      v-for="(image, index) in pj.image"
                      :key="`${pj.id}_image_${index}`"
                    >
                      <img :src="image" />
                    </slide>
                  </carousel>
                  <md-card-actions class="text-center">
                    <md-button
                      v-if="pj.github"
                      :href="pj.guthub"
                      target="_blank"
                      class="md-just-icon md-simple"
                    >
                      <i class="fab fa-github-square" />
                    </md-button>
                    <md-button
                      v-if="pj.demo"
                      :href="pj.demo"
                      target="_blank"
                      class="md-just-icon md-simple"
                    >
                      <i class="fas fa-external-link-square-alt" />
                    </md-button>
                  </md-card-actions>
                </md-card>
                <p>{{ pj.content }}</p>
                <div
                  v-for="(tag, index) in pj.tag"
                  :key="`${pj.id}_tag_${index}`"
                  class="badge badge-success"
                >
                  {{ tag }}
                </div>
                <md-card-actions class="text-center">
                  {{ pj.project_date }} ({{ pj.weeks }} weeks)
                </md-card-actions>
              </template>
            </modal>
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
    Tabs,
    Modal
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
        tag: ["Vue", "MATERIAL"],
        project_date: this.getDate(2020, 12, null),
        weeks: 2,
        github: "https://github.com/isis1234/isis1234_portfolio",
        demo: "https://isis1234.github.io/isis1234_portfolio/"
      },
      {
        id: "pj_yuyu_telegram_bot",
        title: "Yu Telegram Bot",
        modal: false,
        content:
          "A reservation bot for remind you have a sit in the restaurant.",
        image: [
          require("@/assets/img/project_items/YuyuTelegramBot/1.png"),
          require("@/assets/img/project_items/YuyuTelegramBot/2.png"),
          require("@/assets/img/project_items/YuyuTelegramBot/3.png")
        ],
        tag: ["NodeJS", "Telegram Bot"],
        project_date: this.getDate(2020, 10, null),
        weeks: 2,
        github: "https://github.com/isis1234/yuyu_telegram_bot",
        demo: "https://telegram.me/yuyu_test_bot"
      },
      {
        id: "pj_MSDisplayAdapterE6",
        title: "MSDisplayAdapter_E6",
        modal: false,
        content:
          "A script that auto start wireless projecter when i turnon my laptop.",
        image: [
          require("@/assets/img/project_items/MSDisplayAdapter_E6/1.gif")
        ],
        tag: ["Python", "Bat", "Window10", "Sony MP-CD1"],
        project_date: this.getDate(2019, 12, null),
        weeks: 1,
        github: "https://github.com/isis1234/MSDisplayAdapter_E6"
      }
    ];

    let hardware = [];

    let speaker = [];

    return { software, hardware, speaker };
  },
  methods: {
    getDate(year, month, day) {
      let date = new Date(year, month - 1, day);
      let dateStrParts = date.toString().split(" ");

      if (year && month && !day) {
        return `${dateStrParts[1]}, ${dateStrParts[3]}`;
      } else if (year && month && day) {
        return `${date.getDate()} ${dateStrParts[1]}, ${dateStrParts[3]}`;
      } else if (!year && !month && !day) {
        return "Now";
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
