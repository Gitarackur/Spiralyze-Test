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
        <span class="title-transparent-black">WE</span> &nbsp; UNDERSTAND
      </h3>
    </div>

    <div>
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
            </div>
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
</style>
