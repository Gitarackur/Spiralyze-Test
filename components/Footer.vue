<template>
  <div class="">
    <div class="lg:flex lg:items-stretch bg-#194D44">
      <div class="lg:w-6/12 left-footer c-white px-4 md:px-6 lg:px-32 md:py-16">
        <div class="">
          <div class="py-12">
            <h1><span>WATCH </span><span>THE VIDEO</span></h1>
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
                <p>
                  {{ data.content }}
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- <div class="absolute right-0">
          <div class="absolute -right-2">
            <svg
              width="755"
              height="648"
              viewBox="0 0 755 648"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M0 0H719.719C635.252 274 831.175 323.5 719.719 648H0V0Z"
                fill="url(#paint0_linear_1_237)"
              />
              <defs>
                <linearGradient
                  id="paint0_linear_1_237"
                  x1="377.5"
                  y1="0"
                  x2="377.5"
                  y2="648"
                  gradientUnits="userSpaceOnUse"
                >
                  <stop stop-color="#305D52" />
                  <stop offset="1" stop-color="#153F38" />
                </linearGradient>
              </defs>
            </svg>
          </div>

          <div class="absolute right-0">
            <svg
              width="779"
              height="648"
              viewBox="0 0 779 648"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M0 0H742.597C655.445 274 857.597 323.5 742.597 648H0V0Z"
                fill="white"
                fill-opacity="0.2"
              />
            </svg>
          </div>
        </div> -->
      </div>

      <div class="lg:w-6/12 right-footer">
        <div class="h-full w-full">
          <div class="w-full h-full">
            <div class="flex items-center justify-center w-full h-full md:pt-1">
              <div class="h-full flex items-center justify-center">
                <div class="relative cursor-pointer">
                  <div class="absolute position-center">
                    <svg
                      width="208"
                      height="208"
                      viewBox="0 0 208 208"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <circle
                        cx="104"
                        cy="104"
                        r="104"
                        fill="#5BC8AF"
                        fill-opacity="0.1"
                      />
                      <circle
                        cx="104"
                        cy="104"
                        r="103"
                        stroke="white"
                        stroke-opacity="0.3"
                        stroke-width="2"
                      />
                    </svg>
                  </div>

                  <div class="absolute position-center">
                    <svg
                      width="122"
                      height="122"
                      viewBox="0 0 122 122"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <circle
                        cx="61"
                        cy="61"
                        r="59.2692"
                        fill="#5BC8AF"
                        fill-opacity="0.8"
                        stroke="white"
                        stroke-width="2"
                      />
                    </svg>
                  </div>

                  <div class="absolute position-center">
                    <svg
                      width="31"
                      height="36"
                      viewBox="0 0 31 36"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        d="M29.1234 15.1493C31.2086 16.3532 31.2086 19.3629 29.1234 20.5668L4.78475 34.6187C2.69953 35.8226 0.0930175 34.3177 0.0930176 31.9099L0.0930188 3.80613C0.0930189 1.39833 2.69954 -0.106538 4.78475 1.09736L29.1234 15.1493Z"
                        fill="white"
                      />
                    </svg>
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
}

.right-footer {
  width: 100%;
  background-image: url(~~/static/images/video-img.png);
  background-repeat: no-repeat;
  background-size: 100% 100%;
  color: #fff;
}

.position-center {
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
