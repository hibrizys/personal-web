<template>
    <div class="hibrizy_tm_section" id="portfolio">
      <div class="section_inner">
        <div class="hibrizy_tm_portfolio swiper-section">
          <div class="hibrizy_tm_main_title">
            <h3>My <span class="coloring">Projects</span></h3>
          </div>
          <div class="portfolio_list gallery_zoom">
            <swiper
              :loop="false"
              :slidesPerView="1"
              :spaceBetween="0"
              :loopAdditionalSlides="1"
              :autoplay="{
                delay: 6000
              }"
              :navigation="{
                nextEl: '.my_next',
                prevEl: '.my_prev'
              }"
              :pagination="pagination"
              :breakpoints="{
                700: {
                  slidesPerView: 2,
                  spaceBetween: 20
                },
                1200: {
                  slidesPerView: 3,
                  spaceBetween: 30
                }
              }"
              @slideChange="onSlideChange"
              :modules="modules"
              class="swiper-container"
            >
              <swiper-slide class="swiper-slide">
                <div class="list_inner">
                  <div class="image">
                    <img :src="require('@/assets/img/thumbs/1-1.jpg')" alt="" />
                    <div class="main" :data-img-url="require('@/assets/img/portfolio/Project1.png')"></div>
                  </div>
                  <div class="details">
                    <h3>Personal Website</h3>
                    <span>Hibrizy Sulistiyo</span>
                  </div>
                  <a class="hibrizy_tm_full_link portfolio_popup" href="#"></a>
  
                  <!-- Portfolio Popup Informations -->
                  <div class="hibrizy_tm_hidden_content">
                    <div class="portfolio_popup_details">
                      <div class="top_image">
                        <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                        <div
                          class="main"
                          :data-img-url="require('@/assets/img/portfolio/Project1.png')"
                          style="background-image: url('@/assets/img/portfolio/Project1.png')"
                        ></div>
                      </div>
                      <div class="details">
                        <h3>Personal Website</h3>
                        <span>Hibrizy Sulistiyo</span>
                      </div>
                      <div class="text">
                        <br>
                        <p>
                          My personal website, showcases my journey, projects, skills, and experiences. 
                          It serves as a platform to share my passion, highlight my achievements, and connect with like-minded individuals in the tech community. 
                          Through this website, I aim to inspire others, contribute to open-source projects, and continue learning and growing.
                        </p>
                      </div>
                      <div class="additional_images">
                        <ul class="gallery_zoom">
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project1-2.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project1-2.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project1-3.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project1-3.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project1-4.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project1-4.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                        </ul>
                      </div>
                    </div>
                  </div>
                  <!-- /Portfolio Popup Informations -->
                </div>
              </swiper-slide>
              <swiper-slide class="swiper-slide">
                <div class="list_inner">
                  <div class="image">
                    <img :src="require('@/assets/img/thumbs/1-1.jpg')" alt="" />
                    <div class="main" :data-img-url="require('@/assets/img/portfolio/Project2.png')"></div>
                  </div>
                  <div class="details">
                    <h3>CICD Nutanix Platform</h3>
                    <span>PT. Tabel Data Informatika</span>
                  </div>
                  <a class="hibrizy_tm_full_link portfolio_popup" href="#"></a>
  
                  <!-- Portfolio Popup Informations -->
                  <div class="hibrizy_tm_hidden_content">
                    <div class="portfolio_popup_details">
                      <div class="top_image">
                        <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                        <div
                          class="main"
                          :data-img-url="require('@/assets/img/portfolio/Project2-2.png')"
                          style="background-image: url('@/assets/img/portfolio/Project2-2.png')"
                        ></div>
                      </div>
                      <div class="details">
                        <h3>CICD Nutanix Platform</h3>
                        <span>PT. Tabel Data Informatika</span>
                      </div>
                      <div class="text">
                        <br>
                        <p>
                          This study case demonstrates the implementation of a basic CI/CD pipeline for a Spring Boot application. 
                          The goal is to automate the build, test, and deployment processes, 
                          enabling a more efficient and reliable software development lifecycle.
                        </p>
                        <p>
                          My Repository: <a href="https://github.com/hibrizys/CICD_Nutanix" style="color:white">CICD_Nutanix</a>
                        </p>
                      </div>
                      <div class="additional_images">
                        <ul class="gallery_zoom">
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project2-4.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project2-4.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project2-3.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project2-3.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project2-5.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project2-5.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                        </ul>
                      </div>
                    </div>
                  </div>
                  <!-- /Portfolio Popup Informations -->
                </div>
              </swiper-slide>
              <swiper-slide class="swiper-slide">
                <div class="list_inner">
                  <div class="image">
                    <img :src="require('@/assets/img/thumbs/1-1.jpg')" alt="" />
                    <div class="main" :data-img-url="require('@/assets/img/portfolio/Project3.png')"></div>
                  </div>
                  <div class="details">
                    <h3>PlayCourt</h3>
                    <span>PT. Telekomunikasi Indonesia</span>
                  </div>
                  <a class="hibrizy_tm_full_link portfolio_popup" href="#"></a>
  
                  <!-- Portfolio Popup Informations -->
                  <div class="hibrizy_tm_hidden_content">
                    <div class="portfolio_popup_details">
                      <div class="top_image">
                        <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                        <div
                          class="main"
                          :data-img-url="require('@/assets/img/portfolio/Project3-2.png')"
                          style="background-image: url('@/assets/img/portfolio/Project3-2.png')"
                        ></div>
                      </div>
                      <div class="details">
                        <h3>PlayCourt</h3>
                        <span>PT. Telekomunikasi Indonesia</span>
                      </div>
                      <div class="text">
                        <br>
                        <p>
                          PlayCourt is a comprehensive application development platform specifically designed for the development of Telkom Indonesia's digital products.
                        </p>
                        <p>
                          My Jobdesc is to Develop Web Landing Page Playcourt:
                        </p>
                        <ul>
                          <li>Build Web Landing Page as Image Docker and Deploy to Google Kubernetes Engine on Google Cloud Platform</li>
                          <li>Create Web Landing Page Using JavaScript Vue JS include Unit Test Component with Jest</li>
                        </ul>
                        <br>
                        <p>
                          My Work: <a href="https://playcourt.netlify.app/#/" style="color:white">Before Deploy</a>
                        </p>                        
                        <p>
                          Deploy to public: <a href="https://playcourt.id/#/" style="color:white">After Deploy</a>
                        </p>
                      </div>
                      <div class="additional_images">
                        <ul class="gallery_zoom">
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project3-3.jpg')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project3-3.jpg')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project3-4.jpg')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project3-4.jpg')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project3-5.jpg')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project3-5.jpg')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project3-6.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project3-6.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                        </ul>
                      </div>
                    </div>
                  </div>
                  <!-- /Portfolio Popup Informations -->
                </div>
              </swiper-slide>
              <swiper-slide class="swiper-slide">
                <div class="list_inner">
                  <div class="image">
                    <img :src="require('@/assets/img/thumbs/1-1.jpg')" alt="" />
                    <div class="main" :data-img-url="require('@/assets/img/portfolio/Project4.png')"></div>
                  </div>
                  <div class="details">
                    <h3>Capstone</h3>
                    <span>Bangkit Academy 2023 By Google, GoTo, Traveloka</span>
                  </div>
                  <a class="hibrizy_tm_full_link portfolio_popup" href="#"></a>
  
                  <!-- Portfolio Popup Informations -->
                  <div class="hibrizy_tm_hidden_content">
                    <div class="portfolio_popup_details">
                      <div class="top_image">
                        <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                        <div
                          class="main"
                          :data-img-url="require('@/assets/img/portfolio/Project4-2.png')"
                          style="background-image: url('@/assets/img/portfolio/Project4-2.png')"
                        ></div>
                      </div>
                      <div class="details">
                        <h3>Capstone</h3>
                        <span>Bangkit Academy 2023 By Google, GoTo, Traveloka</span>
                      </div>
                      <div class="text">
                        <br>
                        <p>
                          I participated in the Bangkit Academy 2023 Batch 1 By Google, GoTo, Traveloka. 
                          Bangkit Academy is a career readiness program designed by Google to provide Indonesian students with direct exposure to industry practitioners and prepare them with relevant skills for successful careers in leading technology companies. 
                          This program is a career readiness program led by Google, GoTo, and Traveloka.
                        </p>
                        <p>
                          I chose the "Cloud Computing" Learning Path where I worked on:
                        </p>
                        <ul>
                          <li>Completing the Google Cloud Skills Boost Course on Google Cloud Computing Foundations, Cloud Engineer Learning Path, and Google Cloud Skills Boost Quests</li>
                          <li>Learning on Dicoding about Javascript programming, web programming, Making Backend App with Google Cloud, Google Cloud Engineer</li>
                          <li>Completing the Google IT Support course on Coursera</li>
                          <li>Learning Soft Skills & Career Development</li>  
                        </ul>
                        <br>
                        <p>
                          Additionally, I was assigned to a team to work on the "Product Capstone", where we developed an Android application called "Tookar". 
                          Tookar is an app designed to encourage sustainable and environmentally friendly behavior among users by facilitating the exchange of surplus items that might otherwise be discarded as waste.
                        </p>                      
                        <p>
                          During the development of "Product Capstone", I worked on:
                        </p>
                        <ul>
                          <li>Created the GitHub Repository for the Bangkit Team Project</li>
                          <li>Created API with Express JS</li>
                          <li>Tested Endpoint API using Postman</li>
                          <li>Created the Project on Google Cloud Platform</li>  
                          <li>Created the Database on Cloud SQL</li>  
                          <li>Connected the Cloud SQL Database to the API</li>  
                          <li>Configured Google App Engine</li>  
                          <li>Deployed the API to Google App Engine</li>  
                          <li>Created Image Classification with Vertex AI</li>  
                          <li>Produced Documentation on the GitHub Repository Project Product Capstone.</li>  
                        </ul>          
                        <br>                             
                        <p>
                          My Google Cloud Skills Boost Badges: <a href="https://www.cloudskillsboost.google/public_profiles/69d92467-008a-4d12-9472-65ee91f7bc9f" style="color:white">Google Cloud Skills Boost Badges</a>
                        </p>                        
                        <p>
                          My Dicoding Certificates for the courses completed: <a href="https://www.dicoding.com/users/hibrizys/academies?graduation_status=graduated" style="color:white">Dicoding Certificates Course</a>
                        </p>                        <p>
                          The Tookar Project can be found on GitHub: <a href="https://github.com/hibrizys/Tookar" style="color:white">Tookar Project</a>
                        </p>
                      </div>
                      <div class="additional_images">
                        <ul class="gallery_zoom">
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project4-3.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project4-3.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project4-4.jpg')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project4-4.jpg')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project4-5.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project4-5.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project4-6.jpg')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project4-6.jpg')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project4-7.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project4-7.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                          <li>
                            <div class="list_inner">
                              <div class="image">
                                <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                                <div class="main" :data-img-url="require('@/assets/img/portfolio/Project4-8.png')"></div>
                                <a
                                  class="hibrizy_tm_full_link zoom"
                                  :href="require('@/assets/img/portfolio/Project4-8.png')"
                                ></a>
                              </div>
                            </div>
                          </li>
                        </ul>
                      </div>
                    </div>
                  </div>
                  <!-- /Portfolio Popup Informations -->
                </div>
              </swiper-slide>
              <div class="hibrizy_tm_swiper_progress fill">
                <div class="my_pagination_in">
                  <span class="current">0</span>
                  <span class="pagination_progress"
                    ><span class="all"
                      ><span
                        style="transform: translate3d(0px, 0px, 0px) scaleX(0.75) scaleY(1)"
                      ></span></span
                  ></span>
                  <span class="total">04</span>
                </div>
                <div class="my_navigation">
                  <ul>
                    <li>
                      <a class="my_prev" href="#"><i class="icon-left-open-1"></i></a>
                    </li>
                    <li>
                      <a class="my_next" href="#"><i class="icon-right-open-1"></i></a>
                    </li>
                  </ul>
                </div>
              </div>
            </swiper>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  // import Swiper core and required modules
  
  // Import Swiper Vue.js components
  import { Navigation, Pagination } from 'swiper'
  import { Swiper, SwiperSlide } from 'swiper/vue'
  import { swiperSliderCustomSlider } from '../utilits'
  
  export default {
    name: `PortfolioComponent`,
    components: {
      Swiper,
      SwiperSlide
    },
    methods: {
      onSlideChange(swiper) {
        this.activeSlider = swiper.activeIndex + 1
      }
    },
    setup() {
      return {
        modules: [Navigation, Pagination],
        pagination: {
          el: '.hibrizy_tm_swiper_progress',
          type: 'custom', // progressbar
          renderCustom: function (swiper, current, total) {
            swiperSliderCustomSlider(current, total)
          }
        }
      }
    }
  }
  </script>
  