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
        <svg class="hero__sun" viewBox="0 0 400 400" aria-hidden="true">
          <!-- Main upper and right-hand brushstroke -->
          <path
            d="
      M 185 35
      C 231 23, 285 49, 323 91
      C 358 129, 376 181, 369 226
      C 365 244, 358 261, 348 274
      L 328 263
      C 341 242, 346 220, 342 194
      C 338 143, 306 95, 268 72
      C 239 54, 208 50, 181 59
      Z
    "
            fill="#E5392D"
          />

          <!-- Lower-left brushstroke -->
          <path
            d="
      M 347 275
      C 319 331, 258 369, 198 368
      C 136 367, 79 331, 54 278
      C 40 247, 38 212, 47 183
      L 69 193
      C 61 223, 68 257, 87 282
      C 111 318, 154 340, 198 341
      C 251 341, 300 308, 327 264
      Z
    "
            fill="#E5392D"
            opacity="0.92"
          />

          <!-- Lighter upper-left brush movement -->
          <path
            d="
      M 49 180
      C 60 117, 102 66, 156 44
      L 165 62
      C 119 84, 84 126, 70 184
      Z
    "
            fill="#E5392D"
            opacity="0.72"
          />

          <!-- Small dry-brush accents -->
          <path
            d="M 82 105 L 101 83 L 96 108 Z"
            fill="#E5392D"
            opacity="0.65"
          />

          <path
            d="M 354 283 L 371 266 L 364 293 Z"
            fill="#E5392D"
            opacity="0.75"
          />

          <path
            d="M 116 339 L 140 353 L 126 350 Z"
            fill="#E5392D"
            opacity="0.5"
          />
        </svg>

        <img
          class="hero__image"
          src="/images/onoda-samurai-cutout.png"
          alt="A samurai wearing weathered traditional Japanese armour, looking towards the headline"
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

/* Artwork positioning */
.hero__visual {
  position: relative;
  isolation: isolate;
}

.hero__image {
  display: block;
  width: 110%;
  max-width: none;
  height: auto;
  margin-left: -10%;
}

/* Vermilion sun */
.hero__sun {
  position: absolute;
  z-index: -1;
  top: 5%;
  right: 5%;
  width: 70%;
  height: auto;
}

/* Desktop layout */
@media (min-width: 768px) {
  .hero__inner {
    grid-template-columns: 1fr 0.85fr;
    gap: 2rem;
    padding: 5rem 3rem;
  }

  .hero__visual {
    min-height: 600px;
  }

  .hero__image {
    width: 145%;
    margin-left: -45%;
  }
}
</style>
