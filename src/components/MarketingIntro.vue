<template>
  <section class="intro-grid section-gap">

    <v-img
      alt="sample alt text"
      class="intro-photo rounded-lg"
      cover
      src="../assets/avatar-1.jpg"
    />

    <v-card
      class="intro-copy lilac-card rounded-lg"
      elevation="0"
    >
      <h2>
        Are you hitting a wall with your digital marketing?
      </h2>

      <p>
        If you're putting hours into creating content and launching
        campaigns but still not seeing results—you're not alone.
        We've helped hundreds of businesses kickstart a strategy
        that delivers leads, conversions, and returning customers.
      </p>
    </v-card>

  </section>
</template>

<style scoped>
.intro-grid {
  display: grid;
  grid-template-columns: 0.9fr 1.3fr;
  gap: 12px;
  margin-top: 28px;
}

.intro-photo {
  min-height: 190px;
  filter: grayscale(1);
}

.intro-copy {
  min-height: 190px;
  padding: 30px 28px;

  display: flex;
  flex-direction: column;
  justify-content: center;
}

.lilac-card {
  background: #b9c1ff !important;
  color: #101221 !important;
}

.intro-copy h2 {
  margin: 0 0 16px;
  font-size: 20px;
  font-weight: 500;
  line-height: 1.15;
  text-align: center;
}

.intro-copy p {
  margin: 0;
  color: #2f3857;
  font-size: 10px;
  line-height: 1.55;
  text-align: center;
}

@media (max-width: 620px) {
  .intro-grid {
    grid-template-columns: 1fr;
  }

  .intro-photo {
    min-height: 220px;
  }

  .intro-copy {
    min-height: auto;
    padding: 26px 22px;
  }
}
</style>
