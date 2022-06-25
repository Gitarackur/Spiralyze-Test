<template>
  <div class="">
    <Jumbotron />
    <FirstSection />
    <SecondSection />
    <ThirdSection />
    <Footer />
  </div>
</template>

<script>
import Jumbotron from '../components/Jumbotron.vue'
import FirstSection from '../components/FirstSection.vue'
import SecondSection from '../components/SecondSection.vue'
import ThirdSection from '../components/ThirdSection.vue'
import Footer from '../components/Footer.vue'
export default {
  name: 'IndexPage',
  components: { Jumbotron, FirstSection, SecondSection, ThirdSection, Footer },
}
</script>
