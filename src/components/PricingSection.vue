<template>
  <section class="packages-section section-gap">
    <h2 class="section-title">
      Watch your business grow with any of our 3 most popular pro packages
    </h2>

    <div class="pricing-grid">
      <v-card
        v-for="plan in plans"
        :key="plan.name"
        class="pricing-card rounded-lg"
        :class="plan.theme"
        elevation="0"
      >
        <div class="plan-heading">
          <h3>{{ plan.name }}</h3>

          <!-- <p v-if="plan.subtitle" class="plan-subtitle">
            {{ plan.subtitle }}
          </p> -->
        </div>

        <!-- Price -->
        <div class="plan-price">
          <span v-if="plan.oldPrice" class="old-price">
            {{ plan.oldPrice }}
          </span>

          <span>{{ plan.price }}</span>
        </div>

        <p v-if="plan.note" class="plan-note">
          {{ plan.note }}
        </p>

        <!-- Features -->
        <ul class="feature-list">
          <li v-for="feature in plan.features" :key="feature">
            <v-icon class="check-icon" icon="mdi-check" size="14" />

            <span>{{ feature }}</span>
          </li>
        </ul>

        <!-- Button -->
        <v-btn
          block
          class="plan-button"
          :class="plan.buttonClass"
          rounded="pill"
          variant="outlined"
        >
          {{ plan.button }}
        </v-btn>
      </v-card>
    </div>
  </section>
</template>

<script setup lang="ts">

  const plans = [
    {
      name: 'Our #1 DIY Digital Marketing Guide',
      price: '$19.99',
      note: 'Donnot miss this limited time offer!',
      theme: 'plan-white',
      button: 'Buy the guide',
      buttonClass: 'plan-outline',

      features: [
        'Set up your site for success with an SEO checklist',
        'Launch your first paid search ads',
        'Uncover the ultimate social media strategy',
        'Uncover the ultimate social media strategy',
        'Uncover the ultimate social media strategy',
      ],
    },

    {
      name: 'VIP Pass to Our Marketing Masters Webinar Group',
      price: '$39.99',
      note: 'Donnot miss this limited time offer!',
      theme: 'plan-peach',
      button: 'Get a VIP pass',
      buttonClass: 'plan-outline',

      features: [
        'Get full access to our upcoming webinar series (regularly $25/session)',
        'Receive guidance on goal setting, budgeting, and positioning',
        'Ask questions in an exclusive marketers\' forum',
        'Ask questions in an exclusive marketers\' forum',
      ],
    },

    {
      name: 'PRO Business Consulting',
      oldPrice: '$200',
      price: '$49.99',
      note: 'Donnot miss this limited time offer!',
      theme: 'plan-cyan',
      button: 'Claim my discount',
      buttonClass: 'plan-dark',

      features: [
        'Get on track with a 1:1 strategy consulting session with one of our experts',
        'Together, we\'ll unpack your current marketing plan—or build a new one',
        'Come away with a fully optimized strategy, ready to deploy',
      ],
    },
  ]

</script>

<style scoped>
.section-gap {
  margin-top: 28px;
}

.section-title {
  max-width: 520px;
  margin: 0 auto 20px;
  text-align: center;
  font-size: 18px;
  line-height: 1.25;
  font-weight: 500;
}

.pricing-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 12px;
}

.pricing-card {
  display: flex;
  flex-direction: column;
  min-height: 350px;
  padding: 24px 20px 20px;
  color: #101221 !important;
}

.plan-white {
  background: #fff !important;
}

.plan-peach {
  background: #eadbd1 !important;
}

.plan-cyan {
  background: #95d8e2 !important;
}

.plan-heading {
  min-height: 48px;
}

.plan-heading h3 {
  margin: 0;
  font-size: 11px;
  line-height: 1.35;
  font-weight: 700;
}

.plan-subtitle {
  margin: 4px 0 0;
  font-size: 9px;
}

.plan-price {
  display: flex;
  align-items: baseline;
  gap: 5px;
  margin: 14px 0 3px;
  font-size: 16px;
  font-weight: 700;
  white-space: nowrap;
}

.old-price {
  font-size: 14px;
  text-decoration: line-through;
  color: #52616d;
}

.plan-note {
  margin: 0 0 12px;
  font-size: 8px;
  font-style: italic;
  color: #42525b;
}

.feature-list {
  list-style: none;
  padding: 0;
  margin: 14px 0 20px;
  flex: 1;
}

.feature-list li {
  display: flex;
  align-items: flex-start;
  gap: 5px;
  margin-bottom: 8px;
  font-size: 9px;
  line-height: 1.45;
}

.check-icon {
  flex: 0 0 auto;
  margin-top: 1px;
}

.plan-button {
  min-height: 34px !important;
  height: auto !important;
  text-transform: none !important;
  letter-spacing: 0 !important;
  font-size: 9px !important;
  white-space: normal !important;
}

.plan-outline {
  color: #101221 !important;
  border-color: #73777e !important;
}

.plan-dark {
  background: #101221 !important;
  color: #fff !important;
  border-color: #101221 !important;
}

@media (max-width: 620px) {
  .pricing-grid {
    grid-template-columns: 1fr;
  }

  .pricing-card {
    min-height: 0;
    padding: 24px;
  }

  .plan-heading {
    min-height: auto;
  }

  .feature-list {
    margin-bottom: 18px;
  }
}
</style>
