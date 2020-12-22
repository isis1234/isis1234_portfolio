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
          from: this.getDate(2018, 5, 30),
          title: 'Graduated from <a href="https://www.cuhk.edu.hk/" target="_blank">CUHK</a>',
          description:
            'Bachelor of Engineering<br />Major in Computer Engineering',
          color: sonivy_color,
          // showDayAndMonth: true
        },
        {
          from: this.getDate(2014, 5, 30),
          title: 'Graduated from <a href="https://www.ive.edu.hk/ivesite/html/en/aboutive.html" target="_blank">IVE (Tsing Yi)</a>',
          description:
            'Higher Diploma in Telecommuications and Networking',
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
