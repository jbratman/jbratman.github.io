---
layout: concept-home
title: "Jeff Bratman | Engineering Portfolio"
permalink: /home-concept/
---

<div class="landing landing--cinematic">
  <div class="landing-shell">
    <nav class="concept-nav" aria-label="Primary navigation">
      <a class="concept-brand" href="#top"><span>JB</span> · Engineering Portfolio</a>
      <div class="concept-nav__links">
        <a href="#featured">Projects</a>
        <a href="#focus">Focus</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>

    <header class="landing-hero" id="top">
      <div class="hero-background" aria-hidden="true">
        <img
          src="{{ '/images/Jeff_aircraft_composite_v3.jpg' | relative_url }}"
          alt=""
        >
      </div>

      <div class="landing-hero__copy">
        <p class="landing-kicker">Jeff Bratman · Aerospace Engineer</p>

        <h1>
          Systems that<br>
          move, fly, and<br>
          think.
        </h1>

        <p class="landing-subtitle">
          I like figuring out how complex systems fit together and turning ideas into something that actually works. Whether it’s an autonomous racecar, an aircraft, or a robotics platform, I’m most engaged when I can design, build, test, and improve the hardware myself.
        </p>

        <div class="hero-actions">
          <a class="concept-button" href="#featured">Explore my work</a>
          <a class="concept-button concept-button--ghost" href="mailto:bratman.jeff@gmail.com">Contact me</a>
        </div>
      </div>
    </header>

    <main>
      <section class="home-section project-section" id="featured">
        <p class="section-kicker">Featured work</p>
        <h2 class="section-heading">Engineering through working hardware.</h2>
        <p class="section-intro">
          Selected projects spanning autonomous vehicles, aircraft design, electromechanical integration, and vehicle dynamics.
        </p>

        <div class="project-rail-wrap">
          <button class="rail-nav rail-nav--left" type="button" aria-label="Previous project">‹</button>

          <div class="project-rail" id="projectRail">
            {% assign featured_projects = site.portfolio | where: "featured", true | sort: "order" %}

            {% for project in featured_projects %}
              <a class="rail-card" href="{{ project.url | relative_url }}">
                <img src="{{ project.card_image | relative_url }}" alt="{{ project.card_title | default: project.title }}">
                <div class="rail-card__content">
                  <p>{{ project.card_category }}</p>
                  <h2>{{ project.card_title | default: project.title }}</h2>

                  {% if project.card_summary %}
                    <small>{{ project.card_summary }}</small>
                  {% endif %}

                  {% if project.card_tags %}
                    <div class="rail-tags">
                      {% for tag in project.card_tags %}
                        <span>{{ tag }}</span>
                      {% endfor %}
                    </div>
                  {% endif %}
                </div>
              </a>
            {% endfor %}
          </div>

          <button class="rail-nav rail-nav--right" type="button" aria-label="Next project">›</button>
          <div class="rail-dots" aria-label="Project selection"></div>
        </div>
      </section>

      <section class="home-section" id="focus">
        <p class="section-kicker">Engineering focus</p>
        <h2 class="section-heading">I work where disciplines meet.</h2>
        <p class="section-intro">
          My strongest work happens at the boundary between mechanical hardware, electronics, software, and real-world testing.
        </p>

        <div class="focus-grid">
          <article class="focus-card">
            <span class="focus-card__number">01 / DESIGN</span>
            <h3>Mechanical Design</h3>
            <p>Turning requirements and packaging constraints into manufacturable, serviceable hardware.</p>
            <ul>
              <li>CAD</li><li>DFM</li><li>Mechanisms</li><li>Rapid Prototyping</li>
            </ul>
          </article>

          <article class="focus-card">
            <span class="focus-card__number">02 / INTEGRATE</span>
            <h3>Systems Integration</h3>
            <p>Connecting structures, sensors, compute, controls, and power into coherent electromechanical systems.</p>
            <ul>
              <li>Robotics</li><li>Autonomy</li><li>Sensor Packaging</li><li>Hardware</li>
            </ul>
          </article>

          <article class="focus-card">
            <span class="focus-card__number">03 / VALIDATE</span>
            <h3>Testing & Analysis</h3>
            <p>Using simulation, instrumentation, and iterative testing to understand performance and improve reliability.</p>
            <ul>
              <li>MATLAB</li><li>Python</li><li>Vehicle Dynamics</li><li>Validation</li>
            </ul>
          </article>
        </div>
      </section>

            <section class="home-section" id="experience">
        <p class="section-kicker">Selected experience</p>
        <h2 class="section-heading">From concept to test day.</h2>

        <div class="experience-list">
          <article class="experience-item">
            <time>2024 — 2025</time>
            <h3>
              Mechanical Systems Lead
              <span>Autonomous Karting Series · Triton AI</span>
            </h3>
            <p>
              Led mechanical development for an autonomous racing platform, including sensor packaging, electrical integration, thermal considerations, serviceability, and brake actuation development.
            </p>
          </article>

          <article class="experience-item">
            <time>2024 — 2025</time>
            <h3>
              Vehicle Dynamics Engineer
              <span>Indy Autonomous Challenge · AI Racing Tech</span>
            </h3>
            <p>
              Built and refined a ChassisSim vehicle model, compared simulation behavior with telemetry, and supported data-driven handling and stability analysis.
            </p>
          </article>

          <article class="experience-item">
            <time>2025</time>
            <h3>
              Aircraft Design &amp; Integration
              <span>UC San Diego Aerospace Capstone</span>
            </h3>
            <p>
              Designed, fabricated, and tested a payload-delivery aircraft and integrated a servo-driven four-bar deployment mechanism validated through analysis and flight testing.
            </p>
          </article>

          <article class="experience-item">
            <time>2025</time>
            <h3>
              Engineering Demonstration
              <span>OpenSauce 2025 · Triton AI</span>
            </h3>
            <p>
              Designed, built, and publicly demonstrated a low-cost autonomous racecar platform at OpenSauce 2025, integrating mechanical hardware, embedded systems, perception, and real-time controls while engaging with thousands of attendees.
            </p>
          </article>
        </div>
      </section>

      <section class="home-section" id="contact">
        <div class="contact-panel">
          <div>
            <p class="section-kicker">Let’s build something</p>
            <h2>Interested in engineering that leaves the screen and works in the real world?</h2>
          </div>
          <div class="contact-links">
            <a href="mailto:bratman.jeff@gmail.com">Email</a>
            <a href="https://www.linkedin.com/in/jeffrey-bratman/">LinkedIn</a>
            <a href="https://github.com/jbratman">GitHub</a>
          </div>
        </div>
      </section>
    </main>

    <footer class="concept-footer">
      <span>© {{ site.time | date: "%Y" }} Jeff Bratman</span>
      <span>Designed, built, tested, and iterated.</span>
    </footer>
  </div>
</div>

<script>
(() => {
  const cards = [...document.querySelectorAll('.rail-card')];
  const dotsContainer = document.querySelector('.rail-dots');
  const left = document.querySelector('.rail-nav--left');
  const right = document.querySelector('.rail-nav--right');

  if (!cards.length || !dotsContainer) return;

  let activeIndex = Math.min(1, cards.length - 1);
  const wrappedIndex = index => (index + cards.length) % cards.length;

  cards.forEach((_, index) => {
    const dot = document.createElement('button');
    dot.type = 'button';
    dot.setAttribute('aria-label', `Show project ${index + 1}`);
    dot.addEventListener('click', () => {
      activeIndex = index;
      updateCarousel();
    });
    dotsContainer.appendChild(dot);
  });

  function updateCarousel() {
    const previousIndex = wrappedIndex(activeIndex - 1);
    const nextIndex = wrappedIndex(activeIndex + 1);

    cards.forEach((card, index) => {
      card.classList.remove('is-visible', 'is-active');
      card.dataset.position = 'hidden';
      card.setAttribute('aria-hidden', 'true');
      card.tabIndex = -1;

      if (index === previousIndex) {
        card.dataset.position = '-1';
        card.classList.add('is-visible');
      }
      if (index === activeIndex) {
        card.dataset.position = '0';
        card.classList.add('is-visible', 'is-active');
        card.setAttribute('aria-hidden', 'false');
        card.tabIndex = 0;
      }
      if (index === nextIndex) {
        card.dataset.position = '1';
        card.classList.add('is-visible');
      }
    });

    [...dotsContainer.children].forEach((dot, index) => {
      dot.classList.toggle('active', index === activeIndex);
      dot.setAttribute('aria-current', index === activeIndex ? 'true' : 'false');
    });
  }

  left?.addEventListener('click', () => {
    activeIndex = wrappedIndex(activeIndex - 1);
    updateCarousel();
  });

  right?.addEventListener('click', () => {
    activeIndex = wrappedIndex(activeIndex + 1);
    updateCarousel();
  });

  document.addEventListener('keydown', event => {
    if (event.key === 'ArrowLeft') left?.click();
    if (event.key === 'ArrowRight') right?.click();
  });

  updateCarousel();
})();
</script>