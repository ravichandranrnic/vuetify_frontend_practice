<template>
  <section class="about-grid section-gap">

    <v-card
      class="about-copy lilac-card rounded-lg"
      elevation="0"
    >
      <h2>About us</h2>

      <p>
        At <strong>InsightEdge</strong>, we're a team of expert
        consultants who know that marketing can be overwhelming.

        Our mission is to empower businesses to build sustainable
        growth through actionable strategies and personalized
        coaching.

        With years of experience in digital marketing, we've guided
        countless businesses toward marketing success—now it's
        your turn.
      </p>
    </v-card>

    <v-img
      class="about-photo rounded-lg"
      src="../assets/avatar-2.jpg"
      alt="Sample Alt Text"
      cover
    />

  </section>
</template>

<style scoped>
.about-grid {
  display: grid;
  grid-template-columns: 1.3fr 0.9fr;
  gap: 12px;
  margin-top: 28px;
}

.about-copy {
  min-height: 190px;
  padding: 28px;

  display: flex;
  flex-direction: column;
  justify-content: center;

  background: #b9c1ff !important;
  color: #101221 !important;
}

.about-copy h2 {
  margin: 0 0 14px;
  font-size: 30px;
  font-weight: 500;
}

.about-copy p {
  margin: 0;
  color: #2f3857;
  font-size: 10px;
  line-height: 1.55;
}

.about-photo {
  min-height: 190px;
  filter: grayscale(1);
}

@media (max-width: 620px) {
  .about-grid {
    grid-template-columns: 1fr;
  }

  .about-photo {
    min-height: 220px;
  }

  .about-copy {
    min-height: auto;
    padding: 26px 22px;
  }
}
</style>