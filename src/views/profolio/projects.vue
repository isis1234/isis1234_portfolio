<template>
  <div id="projects">
    <hr />
    <h2 class="title text-center">Projects</h2>
    <tabs
      :tab-name="['Software', 'Hardware', 'Present']"
      :tab-icon="['camera', 'palette', 'favorite']"
      plain
      nav-pills-icons
      color-button="success"
    >
      <template slot="tab-pane-1">
        <div class="md-layout">
          <div v-if="!software.length" class="md-layout-item text-center">
            <h4>Comming Soon :)</h4>
          </div>
          <div
            v-for="pj in software"
            class="md-layout-item md-xlarge-size-33 md-large-size-33 md-medium-size-33 md-small-size-50 ml-auto"
            :key="pj.id"
          >
            <img
              v-if="!pj.preview_image"
              :src="pj.image[0]"
              class="rounded"
              @click="pj.modal = true"
            />
            <img
              v-if="pj.preview_image"
              :src="pj.preview_image"
              class="rounded"
              @click="pj.modal = true"
            />
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
                <div
                  v-for="(tag, index) in pj.tag"
                  :key="`${pj.id}_tag_${index}`"
                  class="badge badge-success"
                >
                  {{ tag }}
                </div>
                <br />
                <br />
                <p>{{ pj.content }}</p>
                <md-card-actions class="text-center">
                  {{ pj.project_date }} ({{ pj.weeks }} weeks)
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
                  <md-button
                    v-if="pj.youtube"
                    :href="pj.youtube"
                    target="_blank"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-youtube-square" />
                  </md-button>
                </md-card-actions>
              </template>
            </modal>
          </div>
        </div>
      </template>

      <template slot="tab-pane-2">
        <div class="md-layout">
          <div v-if="!hardware.length" class="md-layout-item text-center">
            <h4>Comming Soon :)</h4>
          </div>
          <div
            v-for="pj in hardware"
            class="md-layout-item md-xlarge-size-33 md-large-size-33 md-medium-size-33 md-small-size-50 ml-auto"
            :key="pj.id"
          >
            <img
              v-if="!pj.preview_image"
              :src="pj.image[0]"
              class="rounded"
              @click="pj.modal = true"
            />
            <img
              v-if="pj.preview_image"
              :src="pj.preview_image"
              class="rounded"
              @click="pj.modal = true"
            />
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
                <div
                  v-for="(tag, index) in pj.tag"
                  :key="`${pj.id}_tag_${index}`"
                  class="badge badge-success"
                >
                  {{ tag }}
                </div>
                <br />
                <br />
                <p>{{ pj.content }}</p>
                <md-card-actions class="text-center">
                  {{ pj.project_date }} ({{ pj.weeks }} weeks)
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
                  <md-button
                    v-if="pj.youtube"
                    :href="pj.youtube"
                    target="_blank"
                    class="md-just-icon md-simple"
                  >
                    <i class="fab fa-youtube-square" />
                  </md-button>
                </md-card-actions>
              </template>
            </modal>
          </div>
        </div>
      </template>

      <template slot="tab-pane-3">
        <div class="md-layout">
          <div v-if="!speaker.length" class="md-layout-item text-center">
            <h4>Comming Soon :)</h4>
          </div>
          <div
            v-for="pj in speaker"
            class="md-layout-item md-xlarge-size-33 md-large-size-33 md-medium-size-33 md-small-size-50 ml-auto"
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
        image: [require("@/assets/img/project_items/SelfPortfolio/1.png")],
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
        id: "pj_projector_3d_art",
        title: "SONY Mobile Projector MP-CD1 Protector Part.1",
        modal: false,
        content:
          "A set 3d module. Part 1 for protect the projector, Part 2 for turn projector to 5, 10, 15 degree (working).",
        image: [
          require("@/assets/img/project_items/Project3Dmodule/1.png"),
          require("@/assets/img/project_items/Project3Dmodule/2.png")
        ],
        preview_image: require("@/assets/img/project_items/Project3Dmodule/preview.gif"),
        tag: ["3D Art", "tinkercad"],
        project_date: this.getDate(2020, 2, null),
        weeks: 2,
        demo:
          "https://www.tinkercad.com/dashboard?type=tinkercad&collection=projects&id=7M41HrLPyzt"
      },
      {
        id: "pj_MSDisplayAdapterE6",
        title: "MSDisplayAdapter_E6",
        modal: false,
        content:
          "A script that auto start wireless projecter when i turnon my laptop.",
        preview_image: require("@/assets/img/project_items/MSDisplayAdapter_E6/1.gif"),
        image: [
          require("@/assets/img/project_items/MSDisplayAdapter_E6/1.gif")
        ],
        tag: ["Python", "Bat", "Window10", "Sony MP-CD1"],
        project_date: this.getDate(2019, 12, null),
        weeks: 1,
        github: "https://github.com/isis1234/MSDisplayAdapter_E6"
      },
      {
        id: "pj_the_forest",
        title: "YouTube Video Log",
        modal: false,
        content: "A youtube game log about the game and me and my friends :).",
        image: ["https://i.ytimg.com/vi/Qucz1EUeKwM/hqdefault.jpg"],
        tag: ["Youtube", "OBS", "VSDC", "Discord", "The Forest"],
        project_date: this.getDate(2019, 4, null),
        weeks: 1,
        youtube: "https://www.youtube.com/watch?v=Qucz1EUeKwM"
      }
    ];

    let hardware = [
      {
        id: "pj_racing_tab_tab_machine",
        title: "Racing Tab Tab Machine",
        modal: false,
        content:
          "Used on gaming with friends in a party. Play against with friends who is the fastest to reach the endpoint.",
        preview_image: "https://hackster.imgix.net/uploads/attachments/779321/blob_3Cv4SWE3ln.blob?auto=compress%2Cformat&w=900&h=675&fit=min",
        image: [
          "https://hackster.imgix.net/uploads/attachments/779329/8903c2a5-9483-4648-b8c8-ec832f05012c_qG5GuBSF2i.jpg?auto=compress%2Cformat&w=680&h=510&fit=max",
          "https://hackster.imgix.net/uploads/attachments/779330/1860be3a-0282-44c3-be9f-bdbefed75e2f_5XRmjyqwRO.jpg?auto=compress%2Cformat&w=680&h=510&fit=max", 
          "https://hackster.imgix.net/uploads/attachments/779332/3af1259c-4d54-44c2-95ee-517ee734c601_5OqOXQnCbk.jpg?auto=compress%2Cformat&w=680&h=510&fit=max" 
        ],
        tag: ["Art", "Games", "Toys", "Kids", "Arduino"],
        project_date: this.getDate(2019, 2, null),
        weeks: 12,
        demo:
          "https://create.arduino.cc/projecthub/isis1234/racing-tab-tab-machine-214ff1"
      }
    ];

    let speaker = [];

    return { software, hardware, speaker };
  },
  methods: {
    getDate(year, month, day) {
      let date = new Date(year, month, day);
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
