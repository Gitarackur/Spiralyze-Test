<template>
  <div class="px-4 md:px-6 lg:px-32 md:pt-16 md:pb-32">
    <div class="mt-20 mb-8 lg:mt-0 lg:mb-0 lg:py-8">
      <h3 class="">
        <span class="title-transparent-black">WE</span>
        CAN ORGANIZE EVERYTHING
      </h3>
    </div>

    <div class="md:flex md:flex-wrap md:-mx-5 md:mb-14 lg:mb-0">
      <div class="md:w-full mb-8 lg:mb-0 lg:w-4/12 md:px-5">
        <div>
          <div class="">
            <p class="p-italic">
              <span class="font-800">Interventions</span> should focus on older
              adult’s desire for connectedness, participation and independence.
            </p>
          </div>
        </div>
      </div>

      <div class="md:w-6/12 lg:w-4/12 md:px-5">
        <div>
          <div>
            <p class="">
              Loneliness and social isolation are growing public health concerns
              in our aging society. Whilst these experiences occur across the
              life span, 50% of individuals aged over 60 are at risk of social
              isolation and one-third will experience some degree of loneliness
              later in life. It is vital to reduce loneliness and social
              isolation among older adults.
            </p>
          </div>
        </div>
      </div>

      <div class="md:w-6/12 lg:w-4/12 md:px-5">
        <div>
          <div>
            <p>
              The methodology framework proposed by Asked and O’Malley and
              further developed by Levac, et al. was used to guide the scoping
              review process. A total of 33 reviews met the inclusion criteria,
              evaluating a range of interventions targeted at older people
              residing in the community or institutionalised settings.
            </p>
          </div>
        </div>
      </div>
    </div>

    <div class="md:py-5">
      <div class="md:flex md:flex-wrap md:-mx-5 my-2 md:-my-5">
        <div
          v-for="(q, i) in 6"
          :key="i"
          class="md:w-6/12 lg:w-4/12 py-2 md:px-5 md:py-5"
        >
          <div class="outline-card p-9">
            <p class="">Needs Assessment</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ThirdSection',
}
</script>

<style scoped>
.bg-\#F5F5F5 {
  background: #f5f5f5;
}
.border-8px {
  border-radius: 8px;
}
.outline-card {
  border: 2px solid #5bc8af;
  border-radius: 4px;
  font-weight: 700;
  font-size: 18px;
  line-height: 28px;
  /* or 156% */
  display: flex;
  align-items: center;
  justify-content: center;
  /* text-align: center; */
}

.p-italic {
  font-style: italic;
  font-size: 18px;
  line-height: 28px;
  color: #333333;
}

.font-800 {
  font-weight: 800;
}
</style>
