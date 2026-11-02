<template>
  <section class="faq-section section-gap">
    <h2 class="section-title">Still have questions?</h2>

    <v-container class="faq-container pa-0">
      <v-expansion-panels
        v-model="openFaq"
        variant="accordion"
        :multiple="false"
        elevation="0"
      >
        <v-expansion-panel
          v-for="(faq, index) in faqs"
          :key="faq.question"
          :value="index"
          class="faq-card rounded-lg"
          :class="faq.theme"
        >
          <!-- Question -->
          <v-expansion-panel-title class="faq-question">
            {{ faq.question }}
          </v-expansion-panel-title>

          <!-- Answer -->
          <v-expansion-panel-text class="faq-answer">
            {{ faq.answer }}
          </v-expansion-panel-text>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-container>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const openFaq = ref(0)

const faqs = [
  {
    question: 'How do I receive my package?',
    answer:
      "After purchasing any package, you'll receive an email from us with a link to your guide, webinar info, or a booking link for your 1:1 session.",
    theme: 'faq-peach',
  },
  {
    question: 'Do I have to attend all webinars?',
    answer:
      "No, but we highly recommend it! You'll get the most value by attending all webinars in the series.",
    theme: 'faq-lilac',
  },
  {
    question: "What if I don't learn anything new?",
    answer:
      "We offer a full refund policy if you don't find value in any of our packages—though we've never had to issue one! Our resources are designed to help you succeed.",
    theme: 'faq-cyan',
  },
]
</script>

<style scoped>
.faq-section {
  margin-top: 28px;
}

.section-title {
  margin: 0 auto 18px;
  text-align: center;
  font-size: 18px;
  line-height: 1.25;
  font-weight: 500;
}

.faq-container {
  max-width: 100%;
}

.faq-card {
  margin-bottom: 10px;
  overflow: hidden;
  color: #101221 !important;
}

/* FAQ colors */
.faq-peach {
  background: #eadbd1 !important;
}

.faq-lilac {
  background: #b9c1ff !important;
}

.faq-cyan {
  background: #95d8e2 !important;
}

/* Question */
.faq-question {
  min-height: 54px;
  padding: 12px 18px;
  font-size: 13px;
  font-weight: 500;
}

/* Answer */
.faq-answer {
  font-size: 10px;
  line-height: 1.5;
  color: #384055;
}

/* Remove unwanted expansion-panel background */
.faq-card :deep(.v-expansion-panel__shadow) {
  box-shadow: none;
}

.faq-card :deep(.v-expansion-panel-text__wrapper) {
  padding: 0 18px 16px;
}

.faq-card :deep(.v-expansion-panel-title__overlay) {
  opacity: 0;
}
</style>