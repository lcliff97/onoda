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
            <!-- Procedural brush-edge texture -->
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
          </defs>

          <!-- Main continuous ensō brushstroke -->
          <g filter="url(#brush-texture)">
            <path
              d="
  M 108 78

  C 140 45, 175 30, 215 34
  C 285 38, 342 87, 365 151
  C 388 218, 361 289, 311 330
  C 263 370, 198 378, 143 348
  C 91 321, 55 270, 48 215
  C 45 190, 49 166, 58 145

  C 69 162, 70 191, 77 217
  C 91 264, 123 300, 165 320
  C 209 341, 258 335, 295 307
  C 334 277, 352 222, 337 169
  C 321 115, 278 75, 227 65
  C 188 57, 151 64, 125 88
  C 118 94, 112 101, 108 78

  Z
"
              fill="#E5392D"
            />
          </g>

          <!-- <path
              d="
      M 238 45
      C 281 59, 320 94, 341 137
      L 330 143
      C 306 99, 274 70, 238 59
      Z
    "
              fill="#B92E25"
              opacity="0.24"
            />

            <path
              d="
      M 72 275
      C 94 319, 136 345, 179 352
      L 173 360
      C 128 351, 91 326, 68 288
      Z
    "
              fill="#B92E25"
              opacity="0.2"
            />

          
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
            /> -->

          <!-- 6. Dry-brush texture: fragmented pigment -->
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
