<template>
  <div class="">
    <div class="h-screen flex items-center justify-center">
      <div class="mx-5 md:mx-0 md:w-6/12 card p-6">
        <h1 class="thank-you-title text-center">Thanks for being awesome!</h1>
        <p class="text-center py-10 bold">
          we have recieved your message and would like to thank you for writing
          to us. if your inquiry is urgent, please use the telephone number
          listed below to talk to one of our staff members. Otherwise, we will
          reply to the email as soon as possible
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ThankYouPage',
  components: {},
}
</script>

<style scoped>
.card {
  background: #fff;
  box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.12);
}

.thank-you-title {
  font-family: 'Montserrat-ExtraBold', sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 44px;
  line-height: 52px;
  color: #5bc8af;
}
</style>
