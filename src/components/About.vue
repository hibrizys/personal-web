<template>
    <div class="hibrizy_tm_section" id="about">
      <div class="section_inner">
        <div class="hibrizy_tm_about">
          <div class="left">
            <div class="image">
              <img :src="require('@/assets/img/thumbs/1-1.jpg')" alt="" />
              <div class="main" :data-img-url="require('@/assets/img/about/izy.jpg')"></div>
            </div>
          </div>
          <div class="right">
            <div class="short">
              <h3 class="name">Hibrizy <span class="coloring">Sulistiyo</span></h3>
              <h3 class="job">
                <AnimationText />
              </h3>
            </div>
            <div class="text">
              <p>
                Im <span>Izy</span>. A <span>Fresh Graduate</span> bachelor of <span>Information Technology</span> at <span>Telkom University</span> 
                with experienced in <span>Software Development</span> and interested in <span>Software Architect</span>, 
                <span>Web Development</span> and <span>Cloud Infrastructure</span>. 
              </p>
            </div>
            <div class="hibrizy_tm_button" id="aboutPopup">
              <a href="#">Details</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import AnimationText from './AnimationText.vue'
  export default {
    name: `AboutApp`,
    data() {
      return {
        open: false
      }
    },
    components: {
      AnimationText
    }
  }
  </script>
  
  <style scoped>
  .hibrizy_tm_modalbox {
    top: -90px;
  }
  </style>
  