<template>
  <div class="px-4 md:px-6 lg:px-32 md:py-16">
    <div class="relative">
      <div class="slides">
        <transition-group
          name="slide"
          mode="out-in"
          enter-class="slide-in"
          leave-class="slide-out"
          enter-active-class="animated slide-in-active"
          leave-active-class="animated slide-out-active"
        >
          <div v-for="(slide, i) in slides" :key="slide.idx">
            <div v-if="i + 1 === active" class="">
              <div class="md:flex lg:items-stretch lg:justify-center">
                <div
                  class="md:w-full md:flex md:items-stretch md:mx-4 md:h-full"
                >
                  <div
                    class="md:flex lg:justify-end md:w-4/12 md:px-4 md:h-full"
                  >
                    <div class="md:w-full lg:w-10/12">
                      <img
                        :src="slide.image"
                        class="w-full md:w-full md:h-full border-8px"
                      />
                    </div>
                  </div>

                  <div class="md:w-8/12 md:px-4 md:h-full">
                    <div
                      class="lg:w-11/12 px-8 lg:px-16 py-16 md:py-14 bg-#194D44 c-white"
                    >
                      <div class="flex items-end justify-between mb-4">
                        <h3 class="sub-heading-2 md:mb-4">
                          {{ slide.name }}
                        </h3>

                        <div>
                          <svg
                            width="60"
                            height="47"
                            viewBox="0 0 60 47"
                            fill="none"
                            xmlns="http://www.w3.org/2000/svg"
                          >
                            <path
                              d="M19.5804 21.9794C21.9114 22.9931 23.7296 24.5137 25.035 26.5412C26.3403 28.5686 26.993 30.9647 26.993 33.7294C26.993 37.6922 25.7343 40.9176 23.2168 43.4059C20.6993 45.802 17.4825 47 13.5664 47C9.65035 47 6.38695 45.7559 3.77622 43.2676C1.25874 40.7794 0 37.6 0 33.7294C0 31.8863 0.2331 30.0431 0.699301 28.2C1.1655 26.3569 2.19114 23.5922 3.77622 19.9059L11.8881 0H25.7343L19.5804 21.9794ZM52.5874 21.9794C54.9184 22.9931 56.7366 24.5137 58.042 26.5412C59.3473 28.5686 60 30.9647 60 33.7294C60 37.6922 58.7413 40.9176 56.2238 43.4059C53.7063 45.802 50.4895 47 46.5734 47C42.6573 47 39.3939 45.7559 36.7832 43.2676C34.2657 40.7794 33.007 37.6 33.007 33.7294C33.007 31.8863 33.2401 30.0431 33.7063 28.2C34.1725 26.3569 35.1981 23.5922 36.7832 19.9059L44.8951 0H58.7413L52.5874 21.9794Z"
                              fill="#2A7C6B"
                            />
                          </svg>
                        </div>
                      </div>

                      <p class="italic big-p-quote">
                        {{ slide.content }}
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </transition-group>
      </div>

      <span class="prev" @click="move(-1)">
        <svg
          width="25"
          height="40"
          viewBox="0 0 25 40"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M24.24 35.76L8.47999 20L24.24 4.24L20 -3.70673e-07L-7.78829e-06 20L20 40L24.24 35.76Z"
            fill="#EAEAEA"
          />
        </svg>
      </span>

      <span class="next" @click="move(1)">
        <svg
          width="25"
          height="40"
          viewBox="0 0 25 40"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0.76001 4.24L16.52 20L0.76001 35.76L5.00001 40L25 20L5.00001 0L0.76001 4.24Z"
            fill="#EAEAEA"
          />
        </svg>
      </span>

      <ul class="dots mt-14 lg:-mx-6">
        <li
          v-for="(dot, index) in slides"
          :key="index"
          class="mx-3 lg:mx-6"
          :class="{ active: ++index === active }"
          @click="jump(index)"
        ></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SecondSection',
  components: {},
  data() {
    return {
      slides: [
        {
          idx: 1,
          name: 'Abbie Harvey',
          content:
            'I have been caring for my mom & dad off and on for about 10 years now, and I know the importance of me being there for appointments. Older people need attention, love and care that they truly deserve.',
          image: './images/review.png',
        },
        {
          idx: 2,
          name: 'John Doe',
          content:
            'I have been caring for my mom & dad off and on for about 10 years now, and I know the importance of me being there for appointments. Older people need attention, love and care that they truly deserve.',
          image: './images/review-3.png',
        },
        {
          idx: 3,
          name: 'Annie Abiot',
          content:
            'I have been caring for my mom & dad off and on for about 10 years now, and I know the importance of me being there for appointments. Older people need attention, love and care that they truly deserve.',
          image: './images/review-2.png',
        },
      ],
      active: 1,
    }
  },
  methods: {
    move(amount) {
      let newActive
      const newIndex = this.active + amount
      if (newIndex > this.slides.length) newActive = 1
      if (newIndex === 0) newActive = this.slides.length
      this.active = newActive || newIndex
    },
    jump(index) {
      this.active = index
    },
  },
}
</script>

<style lang="scss" scoped>
$primary: #5bc8af;

.bg-\#F5F5F5 {
  background: #f5f5f5;
}
.border-8px {
  border-radius: 8px;
}
.bg-\#194D44 {
  background: #194d44;
  box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.12);
  border-radius: 0px 8px 8px 0px;
}

/* slideshow */

.prev,
.next {
  position: absolute;
  top: 40%;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-top: -25px;
  margin-left: 25px;
  cursor: pointer;
  line-height: 48px;
  text-align: center;
  text-indent: -2px;
  transition: all 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);

  &:hover {
    transform: scale(1.2);
    svg {
      path {
        fill: #5bc8af;
        color: #5bc8af;
      }
    }
  }

  &:active {
    transform: translate(0, 3px) scale(1.2);
    svg {
      fill: #5bc8af;
      color: #5bc8af;
    }
  }
}

.next {
  right: 0;
  // margin-left: auto;
  // margin-right: 25px;
  text-indent: 2px;
}

.dots {
  display: block;
  width: 100%;
  text-align: center;

  li {
    width: 16px;
    height: 16px;
    border-radius: 50%;
    background: #eaeaea;
    opacity: 1;
    display: inline-block;
    cursor: pointer;
    transition: opacity 0.4s ease-in-out,
      width 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);

    &.active {
      background: $primary;
      // width: 22px;
      // opacity: 1;
    }
  }
}

.slides {
  display: flex;
  height: 100%;
  align-items: center;
  justify-content: center;
  font-weight: bold;

  @media (min-width: 600px) {
  }

  @media (min-width: 900px) {
  }

  .animated {
    transition: all 400ms;
    position: absolute;
    transform: translate(-50%, -50%);
  }

  .slide-in {
    opacity: 0;
    transform: translate(-40%, -50%);
  }

  .slide-in-active {
    transition-delay: 150ms;
  }

  .slide-out {
    opacity: 1;
  }

  .slide-out-active {
    opacity: 0;
    transform: translate(-60%, -50%);
  }
}
</style>
