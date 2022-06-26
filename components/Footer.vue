<template>
  <div class="">
    <div class="lg:flex lg:items-stretch bg-#194D44">
      <div
        class="relative lg:w-6/12 left-footer c-white px-4 md:px-6 lg:px-32 md:py-16"
      >
        <div class="">
          <div class="py-12">
            <h1 class="title text-center lg:text-left">
              <span class="title-transparent">WATCH </span
              ><span>THE VIDEO</span>
            </h1>
          </div>

          <div class="">
            <div
              v-for="(data, i) in footerItems"
              :key="i"
              class="flex items-stretch -mx-3 py-4"
            >
              <div class="px-3">
                <svg
                  width="18"
                  height="14"
                  viewBox="0 0 18 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M5.6 10.6L1.4 6.4L0 7.8L5.6 13.4L17.6 1.4L16.2 0L5.6 10.6Z"
                    fill="#5BC8AF"
                  />
                </svg>
              </div>

              <div class="px-3">
                <h3 class="sub-heading-2 mb-2">{{ data.title }}</h3>
                <p class="footer-p">
                  {{ data.content }}
                </p>
              </div>
            </div>
          </div>
        </div>

        <div class="absolute bottom-0">
          <svg
            width="360"
            height="280"
            viewBox="0 0 360 280"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <g style="mix-blend-mode: color">
              <rect
                x="-2.88379"
                y="-12.9631"
                width="362.884"
                height="305.926"
                rx="4"
                fill="#194D44"
                fill-opacity="0.3"
              />
            </g>
          </svg>
        </div>
      </div>

      <div class="lg:w-6/12 right-footer p-20 md:p-20 lg:p-0">
        <div class="h-full w-full">
          <div class="w-full h-full">
            <div class="flex items-center justify-center w-full h-full md:pt-1">
              <div class="h-full flex items-center justify-center">
                <div class="cursor-pointer">
                  <div class="">
                    <div
                      class="overlay-circle flex items-center justify-center"
                    >
                      <div class="video-play flex items-center justify-center">
                        <svg
                          width="40"
                          height="45"
                          viewBox="0 0 40 45"
                          fill="none"
                          xmlns="http://www.w3.org/2000/svg"
                        >
                          <path
                            d="M37.6192 19.3543C40.2859 20.8939 40.2859 24.7429 37.6192 26.2825L6.4939 44.2528C3.82723 45.7924 0.493896 43.8679 0.493896 40.7887L0.493898 4.84819C0.493898 1.76899 3.82723 -0.155511 6.4939 1.38409L37.6192 19.3543Z"
                            fill="white"
                          />
                        </svg>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <div class=""></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FooterComponent',
  data() {
    return {
      footerItems: [
        {
          title: 'Needs Assessment',
          content:
            'The Advocacy Evaluation Toolkit contains the instruments used to collect data for evaluating the Consumer Voices for Coverage program. ',
        },
        {
          title: 'Insurance Advocacy',
          content:
            'We are committed to advocating for appropriate coverage and payment policies.',
        },
        {
          title: 'Treatment Planning & Placement',
          content:
            'Patients can better understand medical procedures, discharge instructions, etc.',
        },
      ],
    }
  },
}
</script>

<style scoped>
.bg-\#F5F5F5 {
  background: #f5f5f5;
}
.border-8px {
  border-radius: 8px;
}
.bg-\#194D44 {
  color: #fff;
}

.left-footer {
  width: 100%;
  background: linear-gradient(180deg, #305d52 0%, #153f38 100%);
  color: #fff;
  /* background-image: url(~~/static/images/footer-left-bg.svg); */
}

.right-footer {
  width: 100%;
  background-image: url(~~/static/images/video-img.png);
  background-repeat: no-repeat;
  background-size: 100% 100%;
  color: #fff;
}

@media (min-width: 992px) {
  .position-center {
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
}

.footer-p {
  font-family: 'Montserrat-Regular', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 28px;
  color: rgba(255, 255, 255, 0.8);
}

@media (min-width: 992px) {
  .video-play {
    width: 154.15px;
    height: 154.15px;
    background: rgba(91, 200, 175, 0.8);
    border: 2px solid #ffffff;
    border-radius: 50%;
  }

  .overlay-circle {
    width: 228px;
    height: 228px;
    background: rgba(91, 200, 175, 0.1);
    border: 2px solid rgba(255, 255, 255, 0.44);
    border-radius: 50%;
  }
}

@media (max-width: 768px) {
  .video-play {
    width: 98.66px;
    height: 98.66px;
    background: rgba(91, 200, 175, 0.8);
    border: 2px solid #ffffff;
    border-radius: 50%;
  }

  .overlay-circle {
    width: 128px;
    height: 128px;
    background: rgba(91, 200, 175, 0.1);
    border: 2px solid rgba(255, 255, 255, 0.44);
    border-radius: 50%;
  }
}
@media only screen and (min-width: 768px) and (max-width: 992px) {
  .video-play {
    width: 154.15px;
    height: 154.15px;
    background: rgba(91, 200, 175, 0.8);
    border: 2px solid #ffffff;
    border-radius: 50%;
  }

  .overlay-circle {
    width: 200px;
    height: 200px;
    background: rgba(91, 200, 175, 0.1);
    border: 2px solid rgba(255, 255, 255, 0.44);
    border-radius: 50%;
  }
}
</style>
