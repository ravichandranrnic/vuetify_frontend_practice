<template>
  <v-card
    class="final-cta rounded-xl section-gap"
    elevation="0"
  >

    <p class="saving-label">
      Save $150 today
    </p>

    <h2>
      10x your results with a professional marketing mentor
    </h2>

    <p class="cta-description">
      Take advantage of a limited-time offer on the Pro
      Consulting package.
    </p>

    <v-btn
      class="btn-dark final-button"
      rounded="pill"
      @click="showMessage"
    >
      Buy Now for $49
    </v-btn>
  </v-card>
</template>

<script setup>

</script>

<style scoped>
.final-cta {
  margin-top: 28px;
  padding: 26px 28px 28px;

  text-align: center;
  color: #101221 !important;

  background: linear-gradient(
    115deg,
    #b8c5ff 0%,
    #94d7e2 100%
  ) !important;
}

.saving-label {
  margin: 0 0 4px;
  color: #52647a;
  font-size: 12px;
}

.final-cta h2 {
  max-width: 590px;
  margin: 0 auto 10px;

  font-size: clamp(24px, 4vw, 32px);
  font-weight: 500;
  line-height: 1.12;
  letter-spacing: -0.7px;
}

.cta-description {
  margin: 0 0 20px;
  color: #52647a;
  font-size: 10px;
}

.btn-dark {
  background: #101221 !important;
  color: #fff !important;
}

.final-button {
  min-width: 120px !important;
  min-height: 34px !important;
}

@media (max-width: 620px) {
  .final-cta {
    padding: 25px 18px;
  }
}
</style>