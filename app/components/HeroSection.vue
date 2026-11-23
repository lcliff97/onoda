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

        <NuxtLink to="/classes" class="hero__cta">
          BOOK YOUR FREE TRIAL CLASS <span aria-hidden="true">↗</span>
        </NuxtLink>
      </div>

      <div class="hero__visual">
        <svg class="hero__sun" viewBox="0 0 400 400" aria-hidden="true">
          <defs>
            <!-- Original brush-edge distortion -->
            <filter
              id="brush-texture"
              x="-15%"
              y="-15%"
              width="130%"
              height="130%"
              color-interpolation-filters="sRGB"
            >
              <feTurbulence
                type="fractalNoise"
                baseFrequency="0.038"
                numOctaves="2"
                seed="8"
                result="noise"
              />

              <feDisplacementMap
                in="SourceGraphic"
                in2="noise"
                scale="11"
                xChannelSelector="R"
                yChannelSelector="G"
              />
            </filter>

            <!-- Clip the independent pigment layer to the ensō silhouette -->
            <clipPath id="enso-clip">
              <path
                d="
                  M 112 74
                  C 127 59, 147 48, 166 42
                  C 202 28, 244 35, 277 55
                  C 322 82, 355 128, 366 178
                  C 378 229, 356 282, 319 319
                  C 280 358, 223 376, 169 357
                  C 115 339, 72 296, 53 244
                  C 39 207, 42 174, 59 143
                  C 62 138, 66 135, 70 133
                  C 69 142, 68 151, 67 160
                  C 64 177, 68 195, 75 214
                  C 91 258, 119 294, 157 318
                  C 198 344, 246 346, 284 324
                  C 324 302, 350 259, 354 214
                  C 359 166, 338 118, 302 87
                  C 266 56, 219 42, 176 51
                  C 152 56, 131 70, 115 92
                  C 110 86, 108 79, 112 74
                  Z
                "
              />
            </clipPath>

            <!-- Independent pigment texture generator -->
            <filter
              id="pigment-noise"
              x="0%"
              y="0%"
              width="100%"
              height="100%"
              color-interpolation-filters="sRGB"
            >
              <feTurbulence
                type="fractalNoise"
                baseFrequency="0.08"
                numOctaves="3"
                seed="12"
                result="noise"
              />

              <feColorMatrix
                in="noise"
                type="matrix"
                values="
                  0 0 0 0 0.55
                  0 0 0 0 0.08
                  0 0 0 0 0.05
                  0 0 0.45 0 0
                "
              />
            </filter>
          </defs>

          <!-- Main continuous ensō brushstroke -->
          <g filter="url(#brush-texture)">
            <path
              d="
                M 112 74
                C 127 59, 147 48, 166 42
                C 202 28, 244 35, 277 55
                C 322 82, 355 128, 366 178
                C 378 229, 356 282, 319 319
                C 280 358, 223 376, 169 357
                C 115 339, 72 296, 53 244
                C 39 207, 42 174, 59 143
                C 62 138, 66 135, 70 133
                C 69 142, 68 151, 67 160
                C 64 177, 68 195, 75 214
                C 91 258, 119 294, 157 318
                C 198 344, 246 346, 284 324
                C 324 302, 350 259, 354 214
                C 359 166, 338 118, 302 87
                C 266 56, 219 42, 176 51
                C 152 56, 131 70, 115 92
                C 110 86, 108 79, 112 74
                Z
              "
              fill="#E5392D"
            />
          </g>

          <!-- Independent pigment texture, clipped to the ensō shape -->
          <g clip-path="url(#enso-clip)" opacity="0.28">
            <rect
              x="0"
              y="0"
              width="400"
              height="400"
              filter="url(#pigment-noise)"
            />
          </g>

          <!-- Dry-brush details retained for a later refinement pass -->
          <g
            class="hero__sun-dry-brush"
            fill="none"
            stroke="#F2EFE8"
            display="none"
          >
            <!-- Upper-right: broken, irregular pigment -->
            <path
              d="M 270 68 L 277 72 M 283 76 L 290 81"
              stroke-width="2.5"
              stroke-linecap="round"
              opacity="0.75"
            />

            <path
              d="M 321 119 L 326 127 M 331 135 L 335 143"
              stroke-width="2"
              stroke-linecap="round"
              opacity="0.8"
            />

            <path
              d="M 352 194 L 355 202 M 356 210 L 357 217"
              stroke-width="2.5"
              stroke-linecap="round"
              opacity="0.7"
            />

            <!-- Lower-left: scattered dry-brush gaps -->
            <path
              d="M 48 222 L 49 231 M 50 239 L 52 246"
              stroke-width="2.5"
              stroke-linecap="round"
              opacity="0.8"
            />

            <path
              d="M 77 295 L 83 302 M 88 309 L 94 315"
              stroke-width="2"
              stroke-linecap="round"
              opacity="0.7"
            />

            <path
              d="M 154 350 L 163 353 M 172 356 L 180 357"
              stroke-width="2.5"
              stroke-linecap="round"
              opacity="0.65"
            />
          </g>
        </svg>

        <svg
          class="hero__calligraphy"
          viewBox="0 0 120 360"
          role="img"
          aria-label="鍛錬 — disciplined training"
        >
          <title>鍛錬 — Disciplined training</title>

          <text x="60" y="30" class="hero__calligraphy-text">鍛錬</text>

          <rect x="42" y="265" width="36" height="36" class="hero__seal" />

          <text x="60" y="292" class="hero__seal-text">印</text>
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
  font-family: Anton, sans-serif;
  font-size: clamp(4rem, 11vw, 7rem);
  line-height: 0.89;
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

  filter: saturate(0.35) contrast(0.92) brightness(0.98);

  -webkit-mask-image: linear-gradient(
    to bottom,
    black 0%,
    black 94%,
    transparent 100%
  );

  mask-image: linear-gradient(to bottom, black 0%, black 94%, transparent 100%);
}

/* Vermilion sun */
.hero__sun {
  position: absolute;
  z-index: -1;
  top: 5%;
  right: -2%;
  width: 70%;
  height: auto;
}

/* Tablet layout */
@media (min-width: 768px) and (max-width: 1023px) {
  .hero__inner {
    grid-template-columns: 1.05fr 0.95fr;
    gap: 1rem;
    padding: 4rem 2rem 0;
  }

  .hero__title {
    font-size: clamp(3.5rem, 8vw, 5.5rem);
    line-height: 0.89;
  }

  .hero__visual {
    position: relative;
    min-height: 480px;
  }

  .hero__image {
    position: absolute;
    right: 0.5rem;
    bottom: 0;
    width: 155%;
    max-width: none;
    height: auto;
    margin: 0;
  }
}

/* Desktop layout */
@media (min-width: 1024px) {
  .hero__inner {
    grid-template-columns: 1fr 0.85fr;
    gap: 2rem;
    padding: 5rem 3rem 0;
  }

  .hero__visual {
    position: relative;
    min-height: 600px;
  }

  .hero__image {
    position: absolute;
    right: -3rem;
    bottom: 0;
    display: block;
    width: 135%;
    max-width: none;
    height: auto;
    margin: 0;
  }
}

/* Japanese calligraphy */
.hero__calligraphy {
  position: absolute;
  z-index: 2;
  top: 12%;
  left: 2%;
  width: 90px;
  height: 270px;
  overflow: visible;
}

.hero__calligraphy-text {
  writing-mode: vertical-rl;
  text-orientation: upright;
  font-family: "Yuji Syuku", serif;
  font-size: 76px;
  fill: var(--color-ink);
  text-anchor: middle;
}

.hero__seal {
  fill: var(--color-vermilion);
}

.hero__seal-text {
  fill: var(--color-stone);
  font-family: serif;
  font-size: 22px;
  text-anchor: middle;
}

@media (min-width: 768px) {
  .hero__calligraphy {
    left: -4%;
  }
}
</style>
