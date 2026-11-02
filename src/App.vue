<template>
  <v-app>
    <v-main class="site-shell">
      <div class="page-wrap">

        <SiteHeader />

        <HeroSection />

        <MarketingIntro />

        <PricingSection />

        <AboutSection />

        <FAQSection />

        <TestimonialsSection />

        <FinalCTA />

        <SiteFooter />

      </div>
    </v-main>
  </v-app>
</template>

<script setup>
import SiteHeader from './components/SiteHeader.vue'
import HeroSection from './components/HeroSection.vue'
import MarketingIntro from './components/MarketingIntro.vue'
import PricingSection from './components/PricingSection.vue'
import AboutSection from './components/AboutSection.vue'
import FAQSection from './components/FAQSection.vue'
import TestimonialsSection from './components/TestimonialsSection.vue'
import FinalCTA from './components/FinalCTA.vue'
import SiteFooter from './components/SiteFooter.vue'
</script>

<style>
.site-shell {
  min-height: 100vh;
  background: #101221;
  padding: 24px 20px;
}

.page-wrap {
  width: min(100%, 720px);
  margin: 0 auto;
}
</style>