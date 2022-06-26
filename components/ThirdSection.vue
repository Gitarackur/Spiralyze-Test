<template>
  <div class="px-4 md:px-6 lg:px-32 md:pt-16 md:pb-32">
    <div class="mt-20 mb-8 lg:mt-0 lg:mb-0 lg:py-8">
      <h3 class="title-2">
        <span class="title-transparent-black">WE</span> CAN ORGANIZE EVERYTHING
      </h3>
    </div>

    <div class="md:flex md:flex-wrap md:-mx-5 md:mb-14 lg:mb-7">
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
          v-for="(q, i) in cards"
          :key="i"
          class="relative md:w-6/12 lg:w-4/12 py-2 md:px-5 md:py-5"
        >
          <div class="outline-card p-9">
            <p class="big-p-18 text-center flex">
              {{ q.title }}
            </p>

            <div class="ml-2">
              <svg
                width="18"
                height="18"
                viewBox="0 0 18 18"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M0.5 9C0.5 4.30814 4.30814 0.5 9 0.5C13.6919 0.5 17.5 4.30814 17.5 9C17.5 13.6919 13.6919 17.5 9 17.5C4.30814 17.5 0.5 13.6919 0.5 9Z"
                  stroke="#5BC8AF"
                />
              </svg>
            </div>
          </div>

          <div class="absolute flex items-center justify-center">
            <div class="w-9/12 outline-card-details">
              <div class="mt-3 text-xs tooltip-green px-4 py-3">
                <p class="c-white">{{ q.value }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ThirdSection',
  data() {
    return {
      cards: [
        {
          title: 'Needs Assessment',
          value:
            'We’re experienced in our individual crafts and understand how each one of our roles impacts your plan holistically.',
        },
        {
          title: 'Treatment Planning & Placement',
          value:
            'We’re experienced in our individual crafts and understand how each one of our roles impacts your plan holistically.',
        },
        {
          title: 'Transportation & Logistics',
          value:
            'We’re experienced in our individual crafts and understand how each one of our roles impacts your plan holistically.',
        },
        {
          title: 'Insurance Advocacy',
          value:
            'We’re experienced in our individual crafts and understand how each one of our roles impacts your plan holistically.',
        },
        {
          title: 'Employment Advocacy',
          value:
            'We’re experienced in our individual crafts and understand how each one of our roles impacts your plan holistically.',
        },
        {
          title: 'Aftercare Planning',
          value:
            'We’re experienced in our individual crafts and understand how each one of our roles impacts your plan holistically.',
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
.outline-card {
  border: 2px solid #5bc8af;
  border-radius: 4px;
  font-weight: 700;
  font-size: 18px;
  line-height: 28px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}
.outline-card p {
  font-family: 'Montserrat-Bold', sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 18px;
  line-height: 22px;
  color: #333333;
}

.outline-card-details {
  opacity: 0;
  transition: all 0.05s;
}

.outline-card div {
  opacity: 0;
}

.outline-card:hover + div > .outline-card-details {
  opacity: 1;
}
.outline-card:hover p {
  color: #5bc8af;
}
.outline-card:hover div {
  opacity: 1;
}

.p-italic {
  font-family: 'Montserrat-Italic', sans-serif;
  font-style: italic;
  font-size: 18px;
  line-height: 28px;
  color: #333333;
}

.font-800 {
  font-weight: 800;
}

.title-2 span {
  background: #fff;
}
</style>
