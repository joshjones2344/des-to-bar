<template>
  <div class="max-w-7xl m-center pt-20">
    <div
      class="about-me text-center mt-10 md:mt-32"
      data-aos="fade-up"
      data-aos-delay="100"
      data-aos-duration="800"
    >
      <h2 class="text-5xl dark:text-white">Portfolio</h2>
      <span class="f-gray text-sm dark:text-white">Recent Projects</span>
    </div>
    <div
      class="details flex gap-10 justify-center"
      data-aos="fade-left"
      data-aos-delay="500"
      data-aos-duration="600"
    >
      <swiper
        :slidesPerView="3"
        :spaceBetween="0"
        :centeredSlides="true"
        :pagination="{
          clickable: true,
        }"
        :modules="modules"
        :breakpoints="{
          '200': {
            slidesPerView: 1,
          },
          '600': {
            slidesPerView: 2,
            spaceBetween: 25,
          },
          '768': {
            slidesPerView: 3,
          },
        }"
        class="mySwiper"
      >
        <swiper-slide v-for="(project, key) in recent_projects" :key="key">
          <div
            class="custom-card bg-white dark:bg-slate-800 drop-shadow-2xl w-80 h-96 rounded"
          >
            <div class="tools">
              <div class="circle">
                <span class="red box"></span>
              </div>
              <div class="circle">
                <span class="yellow box"></span>
              </div>
              <div class="circle">
                <span class="green box"></span>
              </div>
            </div>
            <div class="card__content p-2 flex flex-col justify-between">
              <div class="flex flex-col gap-2">
                <div class="project-img">
                  <img
                    :src="project.project_logo"
                    alt=""
                    :class="`${project.class} thumbnail m-auto`"
                  />
                </div>
                <div class="title dark:text-white text-2xl font-semibold pt-2">
                  {{ project.name }}
                </div>
                <div class="description text-sm text-gray-400">
                  {{ project.description }}
                </div>
              </div>
              <div class="visit-link flex justify-center">
                <a
                  class="cssbuttons-io-button bg-cyan-500 w-44 cursor-pointer"
                  :href="project.project_link"
                  target="_blank"
                >
                  Open Link
                  <div class="icon">
                    <svg
                      class="text-cyan-500"
                      height="24"
                      width="24"
                      viewBox="0 0 24 24"
                      xmlns="http://www.w3.org/2000/svg"
                      alignment-baseline="2rem"
                    >
                      <path d="M0 0h24v24H0z" fill="none"></path>
                      <path
                        d="M16.172 11l-5.364-5.364 1.414-1.414L20 12l-7.778 7.778-1.414-1.414L16.172 13H4v-2z"
                        fill="currentColor"
                      ></path>
                    </svg>
                  </div>
                </a>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";

import "swiper/css/pagination";

// import required modules
import { Pagination } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },

  setup() {
    return {
      modules: [Pagination],
    };
  },

  data() {
    return {
      recent_projects: [
        {
          name: "Adventure Sales Dashboard",
          project_link: "https://medium.com/@delsonrantael02/adventure-work-sales-analytics-in-power-bi-0e353b8f5ea2",
          project_logo: "https://i.ibb.co/nBRdJZB/Revised-sales-1.png",
          description: "Using Power BI",
          class: "dsg",
        },
        {
          name: "HR Analytics Dashboard",
          project_link: "https://medium.com/@delsonrantael02/hr-analytics-dashboard-using-microsoft-excel-9de976febaaf",
          project_logo:
            "https://i.ibb.co/Y3vCgvx/Final-Hranalytic-dashboard.png",
          description: "Design in Microsoft Excel",
          class: "richardson",
        },
        {
          name: "Philippines SDG",
          project_link: "https://github.com/joshjones2344/Data-engineering-Capstone-888",
          project_logo:
            "https://i.ibb.co/R6db27j/SDG-dashbaord.png",
          description: "A relational database for SDG dashboard using Flask & Python ",
          class: "vwala",
        },

        {
          name: "Breast Cancer Classification",
          project_link: "https://github.com/joshjones2344/binary-classification-breast-cancer-dataset",
          project_logo: "https://arize.com/wp-content/uploads/2021/12/Binary-Classification-Model.png",
          description:
            "Binary Classification Model ML using Python",
          class: "fundspace",
        },
        {
          name: "ABC Dental Clinic Database",
          project_link: "https://github.com/joshjones2344/Creating-ABC-Dental-Clinic-Database",
          project_logo: "https://i.ibb.co/ngxZwJ2/Dental-Clinic.png",
          description:
            "Creating Database using PosgreSQL",
          class: "capitan",
        },
        {
          name: "Data Migration in SQLite3",
          project_link:
            "https://github.com/joshjones2344/Data-migration-using-python",
          project_logo:
            "https://media.licdn.com/dms/image/D4D12AQHcTftU8AWEjQ/article-cover_image-shrink_720_1280/0/1684603870577?e=2147483647&v=beta&t=O1y4zjZlKO1PymNweoueBwro80TOTUiXrcBJXALD87s",
          description:
            "Source to Data Warehouse Migration using python and SQLAlchemy practice",
          class: "cmdi",
        },
      ],
    };
  },
};
</script>

<style scoped>
.custom-card {
  border-radius: 8px;
  z-index: 1;
  height: 27rem;
  width: 100%;
  margin-right: 5px;
  margin-left: 5px;
  margin-bottom: 20px;
  margin-top: 20px;
}

.tools {
  display: flex;
  align-items: center;
  padding: 9px;
}

.circle {
  padding: 0 4px;
}

.box {
  display: inline-block;
  align-items: center;
  width: 10px;
  height: 10px;
  padding: 1px;
  border-radius: 50%;
}

.red {
  background-color: #ff605c;
}

.yellow {
  background-color: #ffbd44;
}

.green {
  background-color: #00ca4e;
}

.swiper {
  width: 100%;
  height: 65vh;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;

  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}



.cssbuttons-io-button {
  color: white;
  font-family: inherit;
  padding: 0.35em;
  padding-left: 1.2em;
  font-size: 17px;
  font-weight: 500;
  border-radius: 0.9em;
  border: none;
  letter-spacing: 0.05em;
  display: flex;
  align-items: center;
  overflow: hidden;
  position: relative;
  height: 2.8em;
  padding-right: 3.3em;
}

.cssbuttons-io-button .icon {
  background: white;
  margin-left: 1em;
  position: absolute;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 2.2em;
  width: 2.2em;
  border-radius: 0.7em;
  right: 0.3em;
  transition: all 0.3s;
}

.cssbuttons-io-button:hover .icon {
  width: calc(100% - 0.6em);
}



.richardson {
height: 13rem !important;
}
.fundspace {
  width: 50% !important ;
}

.fundspace {
  padding-top: 1px;
}

.richardson {
  padding-top: 5px;
}

.bms {
  padding-top: 1rem;
}

.cmdi {
  width: 60% !important;
  padding-top: 40px;
}

.capitan{
  height: 12rem !important;
}
.vwala {
  padding-top: 1px;
  height: 210px !important;
}

.cssbuttons-io-button .icon svg {
  width: 1.1em;
  transition: transform 0.3s;
}

.cssbuttons-io-button:hover .icon svg {
  transform: translateX(0.1em);
}

.cssbuttons-io-button:active .icon {
  transform: scale(0.95);
}

.card__content {
  height: 22rem;
;
}
</style>
