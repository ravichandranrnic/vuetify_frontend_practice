<template>
  <section class="testimonials-section section-gap">

    <h2 class="section-title">
      Here's what other marketers have to say
    </h2>

    <div class="testimonials-grid">

      <v-card
        v-for="review in reviews"
        :key="review.name"
        class="testimonial-card rounded-lg"
        :class="review.theme"
        elevation="0"
      >

        <v-avatar
          size="34"
          class="review-avatar"
        >
          <v-img
            :src="review.avatar"
            :alt="review.name"
          />
        </v-avatar>

        <h3>{{ review.title }}</h3>


        <p class="review-quote">
          "{{ review.quote }}"
        </p>


        <p class="review-author">
          — {{ review.name }}

          <br />

          <span>{{ review.role }}</span>
        </p>

      </v-card>

    </div>
  </section>
</template>

<script setup>
import Avatar1 from '../assets/avatar-1.jpg'
import Avatar2 from '../assets/avatar-2.jpg'

const reviews = [
  {
    avatar:
      Avatar1,

    title: 'It really is the best.',

    quote:
      "If you only buy one guide, buy this one. The ebook walked me through digital marketing basics better than any other resource I've found.",

    name: 'John, Intern',

    role: 'DIY Marketing Guide customer',

    theme: 'review-white',
  },

  {
    avatar:
      Avatar2,

    title: 'Absolutely worth it.',

    quote:
      'I attended every single one of the webinar sessions. I put together a killer strategy this year, thanks to the team!',

    name: 'Simone, Brand Manager',

    role: 'VIP Webinar Pass customer',

    theme: 'review-peach',
  },

  {
    avatar:
      Avatar1,

    title: 'Collected 200+ leads.',

    quote:
      'Between a single 1:1 session and revisions to my annual marketing strategy, I doubled the number of leads I collect each month.',

    name: 'Gale, Small Business Owner',

    role: '1:1 coaching customer',

    theme: 'review-lilac',
  },
]
</script>

<style scoped>
.testimonials-section {
  margin-top: 28px;
}

.section-title {
  margin: 0 auto 18px;
  text-align: center;
  font-size: 18px;
  line-height: 1.25;
  font-weight: 500;
}

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 12px;
  padding: 0 4px;
}

.testimonial-card {
  min-height: 205px;
  padding: 20px;
  color: #101221 !important;
}

.review-white {
  background: #fff !important;
}

.review-peach {
  background: #eadbd1 !important;
}

.review-lilac {
  background: #b9c1ff !important;
}

.review-avatar {
  filter: grayscale(1);
  margin-bottom: 12px;
}

.testimonial-card h3 {
  margin: 0 0 10px;
  font-size: 12px;
  line-height: 1.3;
  font-weight: 700;
}

.review-quote {
  margin: 0 0 14px;
  font-size: 10px;
  line-height: 1.5;
}

.review-author {
  margin: auto 0 0;
  color: #414653;
  font-size: 8px;
  line-height: 1.5;
}

.review-author span {
  font-size: 7px;
}

@media (max-width: 620px) {
  .testimonials-grid {
    grid-template-columns: 1fr;
    padding: 0;
  }

  .testimonial-card {
    min-height: auto;
  }
}
</style>