---
layout: concept-home
title: "Home Concept"
permalink: /home-concept/
---

<section class="landing">
  <header class="landing-hero">
    <p class="landing-kicker">Jeff Bratman · Engineering Portfolio</p>
    <h1>Systems that<br>move, fly, and<br>think.</h1>
    <p class="landing-subtitle">
      Curious by nature, aerospace engineer by training. I enjoy turning ambitious ideas into reliable systems through design, prototyping, and testing.
    </p>
  </header>

  <section class="project-rail-wrap">
    <button class="rail-nav rail-nav--left" aria-label="Previous project">‹</button>

    <div class="rail-header">Featured Work</div>

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

    <button class="rail-nav rail-nav--right" aria-label="Next project">›</button>

    <div class="rail-dots" aria-hidden="true"></div>
  </section>
</section>

<script>
const cards = [...document.querySelectorAll(".rail-card")];
const dotsContainer = document.querySelector(".rail-dots");
const left = document.querySelector(".rail-nav--left");
const right = document.querySelector(".rail-nav--right");

let activeIndex = Math.min(1, cards.length - 1);

cards.forEach((_, index) => {
  const dot = document.createElement("span");

  dot.addEventListener("click", () => {
    activeIndex = index;
    updateCarousel();
  });

  dotsContainer.appendChild(dot);
});

function wrappedIndex(index) {
  return (index + cards.length) % cards.length;
}

function updateCarousel() {
  const previousIndex = wrappedIndex(activeIndex - 1);
  const nextIndex = wrappedIndex(activeIndex + 1);

  cards.forEach((card, index) => {
    card.classList.remove("is-visible", "is-active");
    card.dataset.position = "hidden";

    if (index === previousIndex) {
      card.dataset.position = "-1";
      card.classList.add("is-visible");
    }

    if (index === activeIndex) {
      card.dataset.position = "0";
      card.classList.add("is-visible", "is-active");
    }

    if (index === nextIndex) {
      card.dataset.position = "1";
      card.classList.add("is-visible");
    }
  });

  [...dotsContainer.children].forEach((dot, index) => {
    dot.classList.toggle("active", index === activeIndex);
  });
}

left.addEventListener("click", () => {
  activeIndex = wrappedIndex(activeIndex - 1);
  updateCarousel();
});

right.addEventListener("click", () => {
  activeIndex = wrappedIndex(activeIndex + 1);
  updateCarousel();
});

updateCarousel();
</script>