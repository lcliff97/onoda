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

          <!-- Main brushstroke artwork -->
          <g filter="url(#brush-texture)">
            <!-- 1. Heavy upper-right sweep -->
            <path
              d="
      M 178 38
      C 231 17, 297 48, 342 111
      C 372 153, 386 210, 361 263
      C 357 273, 352 283, 345 292
      L 322 270
      C 344 232, 350 193, 331 150
      C 309 101, 265 62, 219 56
      C 198 53, 178 59, 160 71
      Z
    "
              fill="#E5392D"
            />

            <!-- 2. Broad lower-left sweep -->
            <path
              d="
      M 345 283
      C 322 331, 270 369, 211 373
      C 147 380, 83 345, 53 291
      C 34 257, 31 218, 47 177
      L 72 190
      C 62 218, 68 251, 85 279
      C 109 319, 151 343, 198 345
      C 248 348, 298 317, 323 270
      Z
    "
              fill="#E5392D"
              opacity="0.94"
            />

            <!-- 3. Lighter upper-left brush movement -->
            <path
              d="
      M 48 183
      C 56 127, 96 72, 150 45
      C 158 41, 168 37, 179 34
      L 185 53
      C 169 59, 155 68, 141 78
      C 104 105, 80 143, 70 187
      Z
    "
              fill="#E5392D"
              opacity="0.68"
            />

            <!-- 4. Additional pigment variation -->
            <path
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

            <!-- 5. Small dry-brush accents -->
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
          </g>

          <!-- 6. Dry-brush texture: fragmented pigment -->
          <g class="hero__sun-dry-brush" fill="none" stroke="#F2EFE8">
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
