<template>
    <div class="hibrizy_tm_modalbox" :class="open ? 'opened' : ''">
      <div class="box_inner">
        <div class="close">
          <a href="#" @click="close"><i class="icon-cancel"></i></a>
        </div>
        <div class="description_wrap">
          <div class="about_popup_details">
            <div class="left">
              <div class="left_inner">
                <div class="author">
                  <div class="avatar_image">
                    <img :src="require('@/assets/img/thumbs/1-1.jpg')" alt="" />
                    <div class="main" :data-img-url="require('@/assets/img/about/izy.jpg')"></div>
                  </div>
                  <div class="short">
                    <h3 class="name">
                      {{ aboutData.firstName }}
                      <span class="coloring">{{ aboutData.lastName }}</span>
                    </h3>
                    <h3 class="job">
                      <AnimationText />
                    </h3>
                  </div>
                </div>
                <div class="list">
                  <ul>
                    <li>
                      <div class="list_inner">
                        <i class="icon-user"></i>
                        <span>{{ aboutData.firstName }} {{ aboutData.lastName }}</span>
                      </div>
                    </li>
                    <li>
                      <div class="list_inner">
                        <i class="icon-calendar"></i>
                        <span>{{ aboutData.bithday }}</span>
                      </div>
                    </li>
                    <li>
                      <div class="list_inner">
                        <i class="icon-location"></i>
                        <span
                          ><a href="#" class="href_location">{{ aboutData.address }}</a></span
                        >
                      </div>
                    </li>
                    <li>
                      <div class="list_inner">
                        <i class="icon-phone"></i>
                        <span
                          ><a href="https://wa.me/6282187431330">{{ aboutData.phn }}</a></span
                        >
                      </div>
                    </li>
                    <li>
                      <div class="list_inner">
                        <i class="icon-mail-1"></i>
                        <span
                          ><a :href="`mailto:${aboutData.email}`">{{ aboutData.email }}</a></span
                        >
                      </div>
                    </li>
                    <li>
                      <div class="list_inner">
                        <i class="icon-linkedin-1"></i>
                        <span
                          ><a href="https://www.linkedin.com/in/hibrizys/">{{
                            aboutData.linkedin
                          }}</a></span
                        >
                      </div>
                    </li>
                  </ul>
                </div>
                <div class="hibrizy_tm_button full">
                  <a
                    href="https://drive.usercontent.google.com/download?id=1xvyd-ebgMPASWEAtHmqRWUP43WNh2LXi&export=download&authuser=0&confirm=t&uuid=0dafd2da-da9e-4ea9-ab56-d47e4677a90f&at=APZUnTU_4h2C090AIBqnEa2DMy8Q:1708355993181"
                    download
                    >Download CV</a
                  >
                </div>
              </div>
            </div>
            <div class="right">
              <div class="right_inner">
                <div class="biography">
                  <div class="about_title">
                    <h3>
                      <span>About <span class="coloring">Me</span></span>
                    </h3>
                  </div>
                  <div class="text">
                    <p>
                      Im <span>Izy</span>. A <span>Fresh Graduate</span> bachelor of <span>Information Technology</span> at <span>Telkom University</span> 
                      with experienced in <span>Software Development</span> and interested in <span>Software Architect</span>, 
                      <span>Web Development</span> and <span>Cloud Infrastructure</span>.
                    </p>
                  </div>
                </div>
                <div class="service">
                  <div class="about_title">
                    <h3>
                      <span>Soft <span class="coloring">Skills</span></span>
                    </h3>
                  </div>
                  <div class="list">
                    <ul>
                      <li v-for="(soft, i) in aboutData.softLists" :key="i">
                        <i class="icon-right-dir"></i>{{ soft }}
                      </li>
                    </ul>
                  </div>
                </div>
                <div class="prog_skill">
                  <div class="about_title">
                    <h3>
                      <span>Technical <span class="coloring">Skills</span></span>
                    </h3>
                  </div>
                  <div class="oki_progress">
                    <div
                      class="progress_inner"
                      v-for="(skill, i) in aboutData.skills.technical"
                      :key="i"
                    >
                      <span
                        ><span class="label">{{ skill.name }}</span
                        ><span class="number">{{ skill.value }}</span></span
                      >
                      <div class="background">
                        <div class="bar open">
                          <div class="bar_in" :style="{ width: `100%` }"></div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="lang_skill">
                  <div class="about_title">
                    <h3>
                      <span>Language <span class="coloring">Skills</span></span>
                    </h3>
                  </div>
                  <div class="circular_progress_bar">
                    <ul>
                      <li>
                        <div class="list_inner">
                          <div class="myCircle" data-value="1"></div>
  
                          <div class="title"><span>Indonesia (Native)</span></div>
                        </div>
                      </li>
                      <li>
                        <div class="list_inner">
                          <div class="myCircle" data-value="0.63"></div>
  
                          <div class="title"><span>English (Upper Intermediate)</span></div>
                        </div>
                      </li>
                      <li>
                        <div class="list_inner">
                          <div class="myCircle" data-value="1"></div>
  
                          <div class="title"><span>Manado (Native)</span></div>
                        </div>
                      </li>
                    </ul>
                  </div>
                </div>
                <div class="timeline">
                  <div class="about_title">
                    <h3>
                      <span>Education <span class="coloring">Timeline</span></span>
                    </h3>
                  </div>
                  <div class="list">
                    <ul>
                      <li v-for="(edu, i) in aboutData.education" :key="i">
                        <div class="list_inner">
                          <div class="time">
                            <span>{{ edu.year }}</span>
                          </div>
                          <div class="place">
                            <h3>{{ edu.unv }}</h3>
                            <span>{{ edu.degree }}</span>
                          </div>
                        </div>
                      </li>
                    </ul>
                  </div>
                </div>
                <div class="timeline">
                  <div class="about_title">
                    <h3>
                      <span>Working <span class="coloring">Timeline</span></span>
                    </h3>
                  </div>
                  <div class="list">
                    <ul>
                      <li v-for="(work, i) in aboutData.working" :key="i">
                        <div class="list_inner">
                          <div class="time">
                            <span>{{ work.year }}</span>
                          </div>
                          <div class="place">
                            <h3>{{ work.company }}</h3>
                            <span>{{ work.deg }}</span>
                          </div>
                        </div>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import { Navigation, Pagination } from 'swiper'
  
  import AnimationText from '../AnimationText.vue'
  export default {
    name: `AboutPopup`,
    
    components: {
      AnimationText
    },
    data() {
      return {
        open: false,
        // data
        aboutData: {
          firstName: 'Hibrizy',
          lastName: 'Sulistiyo',
          bithday: '21 Years Old',
          address: 'Bandung, Indonesia',
          phn: '+62 821 8743 1330',
          linkedin: 'hibrizys',
          email: 'hibrizys@gmail.com',
          softLists: [
            'Leadership',
            'Hardwork',
            'Time Management',
            'Creativity',
            'Problem Solving',
            'Teamwork',
            'Adaptability',
            'Analytical Thinking'
          ],
          skills: {
            technical: [
              { name: 'Git', value: '' },
              { name: 'HTML', value: '' },
              { name: 'CSS', value: '' },
              { name: 'Javascript', value: '' },
              { name: 'Golang', value: '' },
              { name: 'C++', value: '' },
              { name: 'PHP (Codeigniter)', value: '' },
              { name: 'Ubuntu', value: '' },
              { name: 'CentOS', value: '' },
              { name: 'Drawio', value: '' },
              { name: 'VueJs', value: '' },
              { name: 'Docker', value: '' },
              { name: 'Kubernetes', value: '' },
              { name: 'Google Cloud Platform', value: '' },
              { name: 'AWS Platform', value: '' },
              { name: 'Nutanix Platform', value: '' },
              { name: 'ExpressJs', value: '' },
              { name: 'PostMan', value: '' },
              { name: 'MySQL/PostgreSQL', value: '' },
              { name: 'Grafana', value: '' },
              { name: 'Prometheus', value: '' },
              { name: 'SonarQube', value: '' },
              { name: 'Nexus OSS', value: '' },
              { name: 'Microsoft Word', value: '' },
              { name: 'Microsoft Excel', value: '' },
              { name: 'Microsoft Powerpoint', value: '' },
              { name: 'Canva', value: '' }
            ],
            language: [
              { name: 'Indonesia', value: '100' },
              { name: 'English', value: '63' },
              { name: 'Manado', value: '100' }
            ]
          },
          education: [
            {
              year: 'Aug 2020 - Mar 2024',
              unv: 'Telkom University',
              degree: 'Bachelor of Information Technology (3.87/4.00)'
            },            
            {
              year: 'Feb 2023 - Jul 2023',
              unv: 'Bangkit Academy led by Google, Tokopedia, Gojek, & Traveloka',
              degree: 'Specializing in Cloud Computing (91.80/100.00)'
            },
          ],
          working: [
            {
              year: 'Sep 2023 - Jan 2024',
              company: 'PT. Tabel Data Informatika',
              deg: 'Platform Engineering'
            },
            {
              year: 'Jul 2023 - Aug 2023',
              company: 'Telkom Indonesia',
              deg: 'Developer Intern'
            },
            {
              year: 'Mar 2023 - Apr 2023',
              company: 'Digital Talent Scholarship',
              deg: 'Cloud Architect'
            },            
            {
              year: 'Sep 2022 - Jan 2023',
              company: 'Telkom University',
              deg: 'Assistant Practicum ( Data Structure )'
            },            
            {
              year: 'Dec 2022',
              company: 'Telkom University',
              deg: 'Assistant Speaker'
            },            
            {
              year: 'Sep 2022',
              company: 'Telkom University',
              deg: 'Orientation Committee for New Students in the Department of Information Technology'
            },            
            {
              year: 'Aug 2022 - Sep 2022',
              company: 'MySkill',
              deg: 'Frontend Website Development'
            },            
            {
              year: 'Mar 2022 - Jul 2022',
              company: 'Telkom University',
              deg: 'Assistant Lecturer ( Programming Algorithm )'
            }
          ]
        }
      }
    },
    methods: {
      close() {
        this.open = false
      }
    },
    mounted() {
      const aboutPopup = document.getElementById('aboutPopup')
      aboutPopup.addEventListener('click', () => {
        this.open = true
      })
  
      const myCircle = document.querySelectorAll('.myCircle')
      myCircle.forEach((circle) => {
        let progress = circle.getAttribute('data-value')
        let span = document.createElement('span')
        span.className = 'number'
        const value = `${progress * 100}%`
        span.innerHTML = value
        circle.appendChild(span)
        circle.style.setProperty('--progress', value)
        circle.setAttribute('aria-valuenow', value)
      })
    },
    setup() {
      return {
        modules: [Navigation, Pagination]
      }
    }
  }
  </script>
  
  <style scoped>
  .testimonial {
    overflow: hidden;
  }
  .owl-carousel.swiper {
    overflow: unset;
  }
  
  .myCircle {
    --hue: 220;
    --holesize: 67%;
    --track-bg: hsl(233, 34%, 92%);
  
    min-width: 110px;
    min-height: 110px;
    display: grid;
    align-items: center;
    justify-items: center;
    place-items: center;
    position: relative;
    margin-bottom: 5px;
  }
  .myCircle::before {
    content: '';
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    border-radius: 50%;
    z-index: -1;
    background: conic-gradient(
      var(--main-color) var(--progress, 0%),
      rgba(255, 255, 255, 0.15) var(--progress, 0%) 100%
    );
  
    mask-image: radial-gradient(transparent var(--holesize), black calc(var(--holesize) + 1px));
  }
  
  .hibrizy_tm_modalbox .about_popup_details .testimonial .list .swiper .swiper-slide .text {
    width: 100%;
    height: auto;
    clear: both;
    float: left;
    position: relative;
    border: 2px solid #333;
    padding: 40px;
    margin-bottom: 30px;
  }
  
  .hibrizy_tm_modalbox .about_popup_details .testimonial .list .swiper .swiper-slide .text:before {
    position: absolute;
    content: '';
    height: 0px;
    width: 0px;
    top: 100%;
    left: 50px;
    border: solid transparent;
    border-top-color: #333;
    border-width: 18px 18px 0px 0px;
  }
  .hibrizy_tm_modalbox .about_popup_details .testimonial .list .swiper .swiper-slide .text:after {
    position: absolute;
    content: '';
    top: 100%;
    left: 50px;
    height: 0px;
    width: 0px;
    border: solid transparent;
    border-top-color: #222;
    border-width: 14px 13px 0px 0px;
    margin-left: 2px;
  }
  .hibrizy_tm_modalbox .about_popup_details .testimonial .list .swiper .swiper-slide .text i {
    position: absolute;
    z-index: 1;
    font-size: 30px;
    top: -29px;
    left: 50px;
    color: var(--main-color);
  }
  </style>
  