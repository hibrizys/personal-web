<template>
    <div class="hibrizy_tm_section" id="news">
      <div class="section_inner">
        <div class="hibrizy_tm_news swiper-section">
          <div class="hibrizy_tm_main_title">
            <h3>Latest <span class="coloring">News</span></h3>
          </div>
          <div class="news_list">
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
              <swiper-slide class="swiper-slide" v-for="(data, i) in newsData" :key="i">
                <div class="list_inner">
                  <div class="image">
                    <img :src="require('@/assets/img/thumbs/4-3.jpg')" alt="" />
                    <div class="main" :data-img-url="data.imgT"></div>
                    <a class="hibrizy_tm_full_link news_popup" href="#"></a>
                  </div>
                  <div class="details">
                    <h3>
                      <a href="#">{{ data.title }}</a>
                    </h3>
                    <span
                      ><a href="#">{{ data.tag }}</a></span
                    >
                  </div>
  
                  <!-- News Popup Informations -->
                  <div class="hibrizy_tm_hidden_content">
                    <div class="news_popup_details">
                      <div class="top_image">
                        <img :src="require('@/assets/img/thumbs/4-2.jpg')" alt="" />
                        <div class="main" :data-img-url="data.img"></div>
                      </div>
                      <div class="news_main_title">
                        <h3>{{ data.title }}</h3>
                        <span><a href="#">{{ data.tag }}</a></span>
                        <div></div>
                      </div>
                      <div class="text">
                        <p v-for="(text, t) in data.des" :key="t">
                          {{ text }}
                        </p>
                        <div class="news_main_title">
                        <span>{{ data.src }} <a href="https://ieeexplore.ieee.org/document/10428947">https://ieeexplore.ieee.org/document/10428947</a></span>
                      </div>
                      </div>
                    </div>
                  </div>
                  <!-- /News Popup Informations -->
                </div>
              </swiper-slide>
              <div class="hibrizy_tm_swiper_progress fill">
                <div class="my_pagination_in">
                  <span class="currentNews">0</span>
                  <span class="pagination_progress"
                    ><span class="all allNews"><span></span></span
                  ></span>
                  <span class="totalNews">04</span>
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
  import { Navigation, Pagination } from 'swiper'
  import { Swiper, SwiperSlide } from 'swiper/vue'
  import { swiperSliderCustomSlider } from '../utilits'
  
  export default {
    name: `NewsComponent`,
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
            swiperSliderCustomSlider(current, total, 'currentNews', 'totalNews', 'allNews')
          }
        }
      }
    },
    data() {
      return {
        newsData: [
          {
            title: 'My Research Paper of ICICyTA 2023 Have Been Successfully Publish to the IEEE Xplore Digital Library',
            imgT: require('@/assets/img/news/news1.jpg'),
            img: require('@/assets/img/news/news1-2.png'),
            tag: 'Achievement',
            des: [
              'I presented my research paper titled "Design and Implementation of Cloud Computing-Based API for Mobile Application Tookar" at The 2023 3rd International Conference on Intelligent Cybernetics Technology & Applications (ICICyTA) held in Bali, Indonesia. The paper is indexed in Scopus and published in the IEEE Xplore digital library.',
              "This research discusses the implementation of database API and machine learning API, specifically Image Classification, in an Android application using Google Cloud Platform, which effectively enhances the application's efficiency and performance. (16 February 2024)",
            ],
            src: 'My Research Publication:'
          }
        ]
      }
    }
  }
  </script>
  