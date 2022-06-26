<template>
  <div class="px-4 md:px-6 lg:px-32 pt-3 md:pt-16 md:pb-32 bg-#F5F5F5">
    <div class="hidden md:block">
      <div class="md:flex md:-mx-5">
        <div class="md:w-4/12 md:px-5">
          <div>
            <div class="pb-8">
              <img
                src="~~/static/images/image-1.png"
                class="w-full md:w-auto md:h-auto border-8px"
              />
            </div>
          </div>
        </div>

        <div class="md:w-4/12 md:px-5">
          <div>
            <div class="pb-8">
              <img
                src="~~/static/images/image-2.png"
                class="w-full md:w-auto md:h-auto border-8px"
              />
            </div>
          </div>
        </div>

        <div class="md:w-4/12 md:px-5">
          <div>
            <div class="pb-8">
              <img
                src="~~/static/images/image-3.png"
                class="w-full md:w-auto md:h-auto border-8px"
              />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="py-8">
      <h3 class="title-2">
        <span class="title-transparent-black">WE</span> UNDERSTAND
      </h3>
    </div>

    <div class="py-16 md:py-0">
      <div class="md:flex md:flex-wrap md:-mx-5">
        <div class="md:w-6/12 lg:w-4/12 md:px-5">
          <div>
            <div>
              <p>
                I have been caring for my mom & dad off and on for about 10
                years now, and I know the importance of me being there for
                appointments. Older people need attention, love and care that
                they truly deserve.
              </p>
            </div>
          </div>
        </div>

        <div class="md:w-6/12 lg:w-4/12 md:px-5">
          <div>
            <div>
              <p>
                Older adults want to play active and meaningful roles in their
                lives, including as part of a social network, a neighborhood,
                and a community. Service providers and policymakers must
                consider that a lack of sense of purpose can become problematic
                as people age. Engaging them in leisure activities and volunteer
                work is important.
              </p>
            </div>
          </div>
        </div>

        <div class="md:w-6/12 lg:w-4/12 md:px-5">
          <div>
            <div>
              <p>
                Older adults want to play active and meaningful roles in their
                lives, including as part of a social network, a neighborhood,
                and a community. Service providers and policymakers must
                consider that a lack of sense of purpose can become problematic
                as people age. Engaging them in leisure activities and volunteer
                work is important.
              </p>

              <div class="hidden lg:block mt-2.5">
                <button
                  class="w-full flex items-center justify-center px-16 py-5 btn-outline inline-block -mx-1"
                >
                  <div class="px-1">92% Success Rate</div>
                  <div class="px-1">
                    <svg
                      width="17"
                      height="14"
                      viewBox="0 0 17 14"
                      fill="none"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M11.3431 0.92888L16.7071 6.29284C17.0976 6.68336 17.0976 7.31653 16.7071 7.70705L11.3431 13.071C10.9526 13.4615 10.3195 13.4615 9.92893 13.071C9.53841 12.6805 9.53841 12.0473 9.92893 11.6568L13.5858 7.99995H0V5.99995H13.5858L9.92893 2.34309C9.53841 1.95257 9.53841 1.3194 9.92893 0.92888C10.3195 0.538355 10.9526 0.538355 11.3431 0.92888Z"
                        fill="#5BC8AF"
                      />
                    </svg>
                  </div>
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="block lg:hidden md:w-6/12 lg:w-4/12 md:px-5">
          <div class="mt-6 mb-20 md:mt-2 md:mb-0">
            <button
              class="w-full flex items-center justify-center px-16 py-5 btn-outline inline-block -mx-1"
            >
              <div class="px-1">92% Success Rate</div>
              <div class="px-1">
                <svg
                  width="17"
                  height="14"
                  viewBox="0 0 17 14"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                    d="M11.3431 0.92888L16.7071 6.29284C17.0976 6.68336 17.0976 7.31653 16.7071 7.70705L11.3431 13.071C10.9526 13.4615 10.3195 13.4615 9.92893 13.071C9.53841 12.6805 9.53841 12.0473 9.92893 11.6568L13.5858 7.99995H0V5.99995H13.5858L9.92893 2.34309C9.53841 1.95257 9.53841 1.3194 9.92893 0.92888C10.3195 0.538355 10.9526 0.538355 11.3431 0.92888Z"
                    fill="#5BC8AF"
                  />
                </svg>
              </div>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FirstSection',
}
</script>

<style scoped>
@media (max-width: 768px) {
  .bg-\#F5F5F5 {
    background: #fff;
  }
}

@media only screen and (min-width: 768px) and (max-width: 992px) {
  .bg-\#F5F5F5 {
    background: #f5f5f5;
  }
}

@media (min-width: 992px) {
  .bg-\#F5F5F5 {
    background: #f5f5f5;
  }
}
.border-8px {
  border-radius: 8px;
}

.title-2 span {
  background: #f5f5f5;
}
</style>
