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
          <div class="md-layout-item md-size-30 ml-auto">
            <div id="pj1">
              <img :src="pj1.image" class="rounded" @click="pj1.modal=true"/>
              <modal v-if="pj1.modal" @close="pj1.modal=false">
                <!-- <self_portofolio /> -->
                <template slot="header">
                  <h4 class="modal-title"><b>PJ1</b></h4>
                  <md-button
                    class="md-simple md-just-icon md-round modal-default-button"
                    @click="pj1.modal=false"
                  >
                    <md-icon>clear</md-icon>
                  </md-button>
                </template>
                <template slot="body">
                  <p>pj1 Far far away.</p>
                </template>
              </modal>
            </div>
            <div id="pj4">
              <img :src="pj4.image" class="rounded" @click="pj4.modal=true"/>
              <modal v-if="pj4.modal" @close="pj4.modal=false">
                <template slot="header">
                  <h4 class="modal-title"><b>PJ4</b></h4>
                  <md-button
                    class="md-simple md-just-icon md-round modal-default-button"
                    @click="pj4.modal=false"
                  >
                    <md-icon>clear</md-icon>
                  </md-button>
                </template>
                <template slot="body">
                  <p>pj4 Far far away.</p>
                </template>
              </modal>
            </div>
          </div>
          <div class="md-layout-item md-size-30 mr-auto">
            <div id="pj2">
              <img :src="pj2.image" class="rounded" @click="pj2.modal=true"/>
              <modal v-if="pj2.modal" @close="pj2.modal=false">
                <template slot="header">
                  <h4 class="modal-title"><b>PJ2</b></h4>
                  <md-button
                    class="md-simple md-just-icon md-round modal-default-button"
                    @click="pj2.modal=false"
                  >
                    <md-icon>clear</md-icon>
                  </md-button>
                </template>
                <template slot="body">
                  <p>pj2 Far far away.</p>
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
          <div class="md-layout-item md-size-30 mr-auto">
            <div id="pj3">
              <img :src="pj3.image" class="rounded" @click="pj3.modal=true"/>
              <modal v-if="pj3.modal" @close="pj3.modal=false">
                <template slot="header">
                  <h4 class="modal-title"><b>PJ3</b></h4>
                  <md-button
                    class="md-simple md-just-icon md-round modal-default-button"
                    @click="pj3.modal=false"
                  >
                    <md-icon>clear</md-icon>
                  </md-button>
                </template>
                <template slot="body">
                  <p>pj3 Far far away.</p>
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
// import { self_portofolio } from "./projects";
export default {
  components: {
    Tabs, Modal,
    // self_portofolio
  },
  data() {
    return {
      pj1: {
        image: require("@/assets/img/examples/studio-1.jpg"),
        modal: false,
      },
      pj2: {
        image: require("@/assets/img/examples/studio-2.jpg"),
        modal: false,
      },
      pj3: {
        image: require("@/assets/img/examples/studio-4.jpg"),
        modal: false,
      },
      pj4: {
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
      ]
    };
  },
  methods: {
    classicModalHide() {
      this.classicModal = false;
    }
  }
};
</script>
