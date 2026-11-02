<template>
  <v-card class="hero-card rounded-xl" elevation="0">
    <div class="avatar-stack">
      <v-avatar class="stack-avatar" size="42">
        <v-img
          alt="Marketing consultant"
          src="../assets/avatar-1.jpg"
        />
      </v-avatar>

      <v-avatar class="stack-avatar avatar-middle" size="52">
        <v-img
          alt="Marketing consultant"
          src="../assets/avatar-2.jpg"
        />
      </v-avatar>

      <v-avatar class="stack-avatar" size="42">
        <v-img
          alt="Marketing consultant"
          src="../assets/avatar-1.jpg"
        />
      </v-avatar>
    </div>

    <h1 class="hero-title">
      Reach more new customers
      <br class="desktop-break" />
      than ever before
    </h1>

    <p class="hero-description">
      Secure your discount on marketing consulting before it's gone. Get a 1:1
      session with our expert consultants for
      <strong>ONLY $49 ($200 value)</strong>
    </p>

    <div class="countdown">
      <div v-for="unit in countdown" :key="unit.label" class="countdown-unit">
        <span class="countdown-number">
          {{ unit.value }}
        </span>

        <span class="countdown-label">
          {{ unit.label }}
        </span>
      </div>
    </div>

    <div class="hero-actions">
      <v-btn class="btn-dark" rounded="pill">
        Claim this offer
      </v-btn>

      <v-btn
        class="btn-outline"
        rounded="pill"
        variant="outlined"
      >
        Choose your package
      </v-btn>
    </div>

  </v-card>
</template>

<script setup lang="ts">
  import { ref } from 'vue'

  const countdown = [
    { value: '0', label: 'DAYS' },
    { value: '12', label: 'HOURS' },
    { value: '16', label: 'MINUTES' },
    { value: '54', label: 'SECONDS' },
  ]

</script>

<style scoped>
.hero-card {
  padding: 28px 36px 30px;
  text-align: center;
  color: #101221;

  background: linear-gradient(115deg, #b8c5ff 0%, #94d7e2 100%) !important;
}

.avatar-stack {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 18px;
}

.stack-avatar {
  border: 2px solid #f5f5f5;
  margin: 0 -5px;
  filter: grayscale(1);
}

.avatar-middle {
  z-index: 2;
}

.hero-title {
  margin: 0 auto 12px;
  font-size: clamp(26px, 4vw, 36px);
  line-height: 1.08;
  font-weight: 500;
  letter-spacing: -1.1px;
}

.hero-description {
  max-width: 530px;
  margin: 0 auto;
  color: #28364b;
  font-size: 12px;
  line-height: 1.55;
}

.hero-description strong {
  display: inline-block;
  color: #101221;
}

.countdown {
  display: flex;
  justify-content: center;
  gap: clamp(20px, 5vw, 44px);
  margin: 28px 0 27px;
}

.countdown-unit {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-width: 35px;
}

.countdown-number {
  font-size: 25px;
  line-height: 1;
  font-weight: 500;
}

.countdown-label {
  margin-top: 4px;
  font-size: 7px;
  font-weight: 700;
}

.hero-actions {
  display: flex;
  justify-content: center;
  gap: 14px;
  flex-wrap: wrap;
}

.btn-dark,
.btn-outline {
  min-width: 165px !important;
  height: 38px !important;
  text-transform: none !important;
  font-size: 10px !important;
  letter-spacing: 0 !important;
}

.btn-dark {
  background: #101221 !important;
  color: #fff !important;
}

.btn-outline {
  color: #101221 !important;
  border-color: #52677e !important;
}

@media (max-width: 620px) {
  .hero-card {
    padding: 26px 18px;
  }

  .hero-title {
    font-size: 27px;
  }

  .desktop-break {
    display: none;
  }
}
</style>
