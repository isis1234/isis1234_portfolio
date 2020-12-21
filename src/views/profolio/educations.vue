<template>
  <div id="educations">
    <hr>
    <h2 class="title text-center">Educations</h2>
    <Timeline
      :timeline-items="dataTimeline"
      :message-when-no-items="messageWhenNoItems"
      order="desc"
    />
  </div>
</template>

<script>
import Timeline from "timeline-vuejs"
export default {
  components: {
    Timeline
  },
  data(){
    // let sonivy_color = this.getRandomColor();
    // let gti_color = this.getRandomColor();
    let now_color = "#e74c3c";
    let sonivy_color = "#2ecc71";
    let gti_color = "#2da1bf";
    return {
      messageWhenNoItems: "No articles found.",
      dataTimeline: [
        {
          from: this.getDate(2018, 10, 2),
          title: 'Graduated from <a href="https://www.sonivy.com/" target="_blank">CUHK</a>',
          description:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius earum architecto dolor, vitae magnam voluptate accusantium assumenda numquam error mollitia, officia facere consequuntur reprehenderit cum voluptates, ea tempore beatae unde.',
          color: sonivy_color,
          // showDayAndMonth: true
        },
        {
          from: this.getDate(2017, 9, 9),
          title: 'Graduated from <a href="https://www.gti.com.hk/" target="_blank">TY IVE</a>',
          description:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius earum architecto dolor, vitae magnam voluptate accusantium assumenda numquam error mollitia, officia facere consequuntur reprehenderit cum voluptates, ea tempore beatae unde.',
          // showDayAndMonth: true,
          color: gti_color
        }
      ]
    }
  },
  methods: {
    getRandomColor() {
      let letters = '0123456789ABCDEF';
      let color = '#';
      for (let i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
      }
      // console.log(color);
      return color;
    },
    getDate(year, month, day) {
      return new Date(year, month - 1, day)
    }
  }
};
</script>
