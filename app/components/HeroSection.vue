<template>
  <section class="hero">
    <div class="hero__inner">
      <div class="hero__content">
        <p class="hero__eyebrow">DISCIPLINE · PRECISION · PROGRESS</p>

        <h1 class="hero__title">
          DISCIPLINE
          <span>BUILDS</span>
          FREEDOM.
        </h1>

        <p class="hero__description">
          Built through practice. Refined through discipline.
        </p>

        <a href="/classes" class="hero__cta">
          BOOK YOUR FREE TRIAL CLASS <span aria-hidden="true">↗</span>
        </a>
      </div>

      <div class="hero__visual">
        <img
          src="/images/onoda-samurai.png"
          alt="A contemplative samurai wearing weathered traditional Japanese armour"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background-color: var(--color-stone);
}

.hero__inner {
  display: grid;
  grid-template-columns: 1fr;
  gap: 3rem;
  padding: 4rem 1.5rem;
}

.hero__content,
.hero__visual {
  min-width: 0;
}

.hero__eyebrow {
  margin: 0 0 1.5rem;
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 0.2em;
  color: var(--color-slate);
}

.hero__title {
  margin: 0;
  font-family: var(--font-display);
  font-size: clamp(4rem, 11vw, 7rem);
  line-height: 0.85;
  letter-spacing: -0.025em;
  text-transform: uppercase;
}

.hero__title span {
  display: block;
  color: var(--color-vermilion);
}

.hero__description {
  margin: 2rem 0 0;
  font-size: 0.9rem;
  line-height: 1.7;
  color: var(--color-slate);
}

.hero__cta {
  display: inline-flex;
  align-items: center;
  gap: 1.5rem;
  margin-top: 2rem;
  padding: 1rem 0;
  border-bottom: 1px solid var(--color-ink);
  color: var(--color-ink);
  font-size: 0.7rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-decoration: none;
}

.hero__cta:hover {
  color: var(--color-vermilion);
  border-color: var(--color-vermilion);
}

@media (min-width: 768px) {
  .hero__inner {
    grid-template-columns: 1fr 0.85fr;
    gap: 2rem;
    padding: 5rem 3rem;
  }

  .hero__visual {
    position: relative;
    min-height: 500px;
  }

  .hero__image {
    display: block;
    width: 100%;
    height: auto;
    object-fit: contain;
  }
}
</style>
