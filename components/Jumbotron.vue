<template>
  <div class="jumbotron relative">
    <Navbar />

    <div
      class="lg:flex lg:items-center pt-11 pb-44 md:pt-16 md:pb-44 lg:py-16 md:my-1 px-4 md:px-32"
    >
      <div class="lg:w-6/12">
        <h1 class="title text-center lg:text-left">
          <span class="title-transparent">GET AN</span>
          <br class="hidden md:block" />
          <span>INTERVENTION</span>
        </h1>

        <p class="text-center lg:text-left my-4 md:mt-4">
          Showing greater respect to older adults can be done in several ways :
          acknowledging and putting to use the talents and skills of older
          adults; creating intergenerational initiatives; and allowing older
          adults to stay active and independent for as long as possible.
        </p>
      </div>

      <div class="lg:flex lg:items-center lg:justify-end lg:w-6/12 lg:pl-6">
        <div
          :key="contactFormKey"
          class="md:w-full lg:w-10/12 contactForm px-4 md:px-7"
        >
          <div class="pt-9 pb-14 md:py-12">
            <div class="pb-9 md:pb-9 flex items-center justify-center">
              <h1 class="sub-heading-1">Contact Us</h1>
            </div>

            <div class="md:flex md:flex-wrap -my-2 md:-m-2">
              <div class="md:w-6/12 py-2 md:p-2">
                <TaskInput
                  v-model="form.firstName"
                  name="FirstName"
                  label="First Name"
                  :error="checkErrorValue('firstName')"
                  :error-message="checkError('firstName')"
                />
              </div>

              <div class="md:w-6/12 py-2 md:p-2">
                <TaskInput
                  v-model="form.lastName"
                  name="lastName"
                  label="Last Name"
                  :error="checkErrorValue('lastName')"
                  :error-message="checkError('lastName')"
                />
              </div>

              <div class="md:w-6/12 py-2 md:p-2">
                <TaskInput
                  v-model="form.businessEmail"
                  name="BusinessEmail"
                  label="Business Email"
                  :error="checkErrorValue('businessEmail')"
                  :error-message="checkError('businessEmail')"
                />
              </div>

              <div class="md:w-6/12 py-2 md:p-2">
                <TaskInput
                  v-model="form.company"
                  name="Company"
                  label="Company"
                  :error="checkErrorValue('company')"
                  :error-message="checkError('company')"
                />
              </div>

              <div class="md:w-full py-2 md:p-2">
                <TaskSelect
                  v-model="form.country"
                  label="-Country-"
                  :error="checkErrorValue('country')"
                  :error-message="checkError('country')"
                >
                  <option value="dhdd">Select Country</option>
                  <option
                    v-for="(country, i) in countries"
                    :key="i"
                    :value="country"
                  >
                    {{ country }}
                  </option>
                </TaskSelect>
              </div>

              <div class="py-2 md:p-2 flex items-center justify-center w-full">
                <div class="pt-5">
                  <button
                    class="flex items-center btn px-16 py-5 inline-block -mx-1"
                    @click="validate"
                  >
                    <div class="px-1">
                      <svg
                        width="21"
                        height="18"
                        viewBox="0 0 21 18"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M0.00999999 18L21 9L0.00999999 0L0 7L15 9L0 11L0.00999999 18Z"
                          fill="white"
                        />
                      </svg>
                    </div>

                    <p class="big-p-18 px-1">Submit</p>
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="hidden lg:block lg:absolute bottom-0">
      <div class="absolute bottom-0" style="overflow: hidden">
        <svg
          width="1440"
          height="111"
          viewBox="0 0 1440 111"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          ``
          <path
            d="M0 68.6766C310 -147.298 926 229.879 1440 68.6766V111H0V68.6766Z"
            fill="#F5F5F5"
            fill-opacity="0.3"
          />
        </svg>
      </div>

      <div class="absolute bottom-0" style="overflow: hidden">
        <svg
          class="transform-svg"
          width="1440"
          height="90"
          viewBox="0 0 1440 90"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0 55.1705C310 -118.33 926 184.67 1440 55.1705V89.1704H0V55.1705Z"
            fill="#F5F5F5"
          />
        </svg>
      </div>
    </div>

    <div
      class="mobile block md:hidden lg:hidden absolute bottom-0 right-0 left-0"
    >
      <div
        class="w-full absolute bottom-0 right-0 left-0"
        style="overflow: hidden"
      >
        <svg
          width="3600"
          height="111"
          viewBox="0 0 3600 111"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0 68.6766C310 -147.298 926 229.879 1440 68.6766V111H0V68.6766Z"
            fill="#F5F5F5"
            fill-opacity="0.3"
          />
        </svg>
      </div>

      <div
        class="w-full absolute -bottom-2 right-0 left-0"
        style="overflow: hidden"
      >
        <svg
          class="transform-svg"
          width="3600"
          height="89"
          viewBox="0 0 3600 89"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0 55.1705C310 -118.33 926 184.67 1440 55.1705V89.1704H0V55.1705Z"
            fill="white"
          />
        </svg>
      </div>
    </div>

    <div
      class="tablet hidden md:block lg:hidden absolute bottom-0 right-0 left-0"
    >
      <div
        class="w-full absolute -bottom-2 right-0 left-0"
        style="overflow: hidden"
      >
        <svg
          width="7680"
          height="111"
          viewBox="0 0 7680 111"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0 68.6766C310 -147.298 926 229.879 1440 68.6766V111H0V68.6766Z"
            fill="#F5F5F5"
            fill-opacity="0.3"
          />
        </svg>
      </div>

      <div
        class="w-full absolute -bottom-2 right-0 left-0"
        style="overflow: hidden"
      >
        <svg
          class="transform-svg-1"
          width="7680"
          height="89"
          viewBox="0 0 7680 89"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M0 55.1705C310 -118.33 926 184.67 1440 55.1705V89.1704H0V55.1705Z"
            fill="#F5F5F5"
          />
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
import Validator from 'fastest-validator'
import countries from '../countries'
import TaskInput from './modules/task-input.vue'
import TaskSelect from './modules/task-select.vue'
import Navbar from './Navbar.vue'

const v = new Validator()

const schema = {
  firstName: { type: 'string', min: 2, optional: false },
  lastName: { type: 'string', min: 2, optional: false },
  businessEmail: { type: 'email', optional: false },
  company: { type: 'string', min: 2, optional: false },
  country: { type: 'string', min: 2, optional: false },
}
const firstNameschema = {
  firstName: { type: 'string', min: 2, optional: false },
}
const lastNameschema = {
  lastName: { type: 'string', min: 2, optional: false },
}
const businessEmailSchema = {
  businessEmail: { type: 'email', optional: false },
}
const companySchema = {
  company: { type: 'string', min: 2, optional: false },
}
const countrySchema = {
  country: { type: 'string', min: 2, optional: false },
}

const check1 = v.compile(firstNameschema)
const check2 = v.compile(lastNameschema)
const check3 = v.compile(businessEmailSchema)
const check4 = v.compile(companySchema)
const check5 = v.compile(countrySchema)
const checkAll = v.compile(schema)

export default {
  name: 'JumbotronComponent',
  components: { TaskInput, TaskSelect, Navbar },
  data() {
    return {
      form: {
        firstName: null,
        lastName: null,
        businessEmail: null,
        company: null,
        country: null,
      },
      onSubmitError: false,
      contactFormKey: 0,
      valiators: [],
      countries,
    }
  },
  computed: {},
  watch: {
    'form.firstName': {
      handler(val, oldVal) {
        this.validators = check1({ firstName: val })
      },
      deep: true,
    },
    'form.lastName': {
      handler(val, oldVal) {
        this.validators = check2({ lastName: val })
      },
      deep: true,
    },
    'form.businessEmail': {
      handler(val, oldVal) {
        this.validators = check3({ businessEmail: val })
      },
      deep: true,
    },
    'form.company': {
      handler(val, oldVal) {
        this.validators = check4({ company: val })
      },
      deep: true,
    },
    'form.country': {
      handler(val, oldVal) {
        this.validators = check5({ country: val })
      },
      deep: true,
    },
    onSubmitError: {
      handler(val, oldVal) {
        if (val === true) {
          this.validators = checkAll(this.form)
        }
      },
      deep: true,
    },
  },
  methods: {
    validate() {
      if (typeof v.validate(this.form, schema) === 'boolean') {
        this.$router.push('/thank-you')
      } else {
        checkAll(this.form)
        this.onSubmitError = true
        this.contactFormKey += 1
      }
    },
    checkError(property) {
      return this.validators &&
        this.validators.length > 0 &&
        this.validators.find((curr) => curr.field === property) &&
        this.validators.find((curr) => curr.field === property).message
        ? this.validators.find((curr) => curr.field === property).message
        : ''
    },
    checkErrorValue(property) {
      return (
        this.validators &&
        this.validators.length > 0 &&
        this.validators.some((curr) => curr.field === property)
      )
    },
  },
}
</script>

<style scoped>
@media (min-width: 992px) {
  .jumbotron {
    width: 100%;
    min-height: 80vh;
    background-image: linear-gradient(
        180deg,
        #194d41 0%,
        rgba(25, 77, 65, 0.7) 100%
      ),
      url(~~/static/images/jumbotron.png);
    mix-blend-mode: multiply;
    background-repeat: no-repeat;
    background-size: 100% 100%;
    color: #fff;
  }
}

/*800px*/
@media only screen and (min-width: 768px) and (max-width: 992px) {
  .jumbotron {
    width: 100%;
    min-height: 80vh;
    background-image: linear-gradient(
        180deg,
        #194d41 0%,
        rgba(25, 77, 65, 0.7) 100%
      ),
      url(~~/static/images/jumbotron.png);
    mix-blend-mode: multiply;
    background-repeat: no-repeat;
    background-size: 100% 100%;
    color: #fff;
  }
}

@media (max-width: 768px) {
  .jumbotron {
    width: 100%;
    min-height: 100vh;
    background-image: linear-gradient(
        180deg,
        #194d41 0%,
        rgba(25, 77, 65, 0.7) 100%
      ),
      url(~~/static/images/jumbotron.png);
    mix-blend-mode: multiply;
    background-repeat: no-repeat;
    background-size: 100% 100%;
    color: #fff;
  }
}

.contactForm {
  background: linear-gradient(180deg, #2a7d6c 0%, rgba(62, 105, 96, 0.62) 100%);
  box-shadow: 0px 10px 50px rgba(0, 0, 0, 0.12);
  border-radius: 12px;
}

.contactForm h2 {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 28px;
  line-height: 34px;
  /* identical to box height */
  display: flex;
  align-items: center;
  text-align: center;
  color: #ffffff;
}

.transform-svg {
  transform: translateY(10px);
  fill: #ffffff;
}

.transform-svg-1 {
  transform: translateY(5px);
  fill: #ffffff;
}
</style>
