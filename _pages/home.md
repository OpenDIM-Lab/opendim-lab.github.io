---
title: "Home"
layout: homelay
excerpt: "OpenDIM Lab — Tactile Sensing, Dexterous Manipulation and Robot Learning"
sitemap: true
permalink: /
---
<!-- ## Welcome to -->

<div style="margin: 20px 0 24px;">
  <img
    src="{{ '/images/logo/lab-logo_2.svg' | relative_url }}"
    alt="OpenDIM Lab logo"
    style="display: block; width: 280px; max-width: 100%; height: auto; margin: 0 auto;">
</div>
<div class="home-intro" markdown="0">
  <p>
    OpenDIM Lab is a robotics research laboratory at Beijing Institute of
    Technology, focusing on tactile sensing, dexterous manipulation, robot
    learning, and embodied intelligence.
  </p>
  <div class="home-actions">
    <a href="{{ '/people/' | relative_url }}">Meet the Team</a>
    <a href="{{ '/research/' | relative_url }}">Explore Our Research</a>
    <a href="{{ '/join-us/' | relative_url }}">Join Us</a>
  </div>
</div>
<style>
.home-intro {
  max-width: 780px;
  margin: 0 auto 28px;
  text-align: center;
}
.home-intro p {
  margin: 0 auto 18px;
  line-height: 1.6;
}
.home-actions {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
}
.home-actions a {
  display: inline-block;
  padding: 8px 14px;
  border: 1px solid #2266aa;
  border-radius: 4px;
  background: #2266aa;
  color: #fff;
  text-decoration: none;
}
.home-actions a:hover,
.home-actions a:focus {
  background: #174a7c;
  color: #fff;
  text-decoration: none;
}
.od-carousel {
  position: relative;
  margin: 20px 0 32px;
  border: 1px solid #e5e7eb;
  border-radius: 8px;
  overflow: hidden;
  background: #fff;
}
.od-project-link {
  display: block;
  color: inherit;
  text-decoration: none !important;
}
.od-project-link:hover { color: inherit; }
.od-media {
  position: relative;
  aspect-ratio: 16 / 9;
  overflow: hidden;
  background: #f5f6f8;
}
.od-media img {
  position: absolute;
  inset: 0;
  display: block;
  width: 100%;
  height: 100%;
  object-fit: contain;
  margin: 0;
  opacity: 0;
  transition: opacity 1000ms ease;
}
.od-media img.is-visible {
  opacity: 1;
}
@media (prefers-reduced-motion: reduce) {
  .od-media img { transition: none; }
}
.od-caption {
  padding: 18px 55px 12px;
  text-align: center;
}
.od-caption h3 {
  margin: 0 0 8px;
  color: #222;
}
.od-caption p {
  margin: 0 0 8px;
  color: #555;
  font-size: 15px;
}
.od-visit { color: #2266aa; font-size: 14px; }
.od-arrow {
  position: absolute;
  top: 30%;
  z-index: 2;
  width: 38px;
  height: 48px;
  padding: 0;
  border: 0;
  border-radius: 4px;
  background: rgba(0,0,0,.5);
  color: #fff;
  font-size: 30px;
  cursor: pointer;
}
.od-prev { left: 10px; }
.od-next { right: 10px; }
.od-controls {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  padding: 12px 10px 18px;
}
.od-dot {
  width: 10px;
  height: 10px;
  padding: 0;
  border: 0;
  border-radius: 50%;
  background: #c8cdd3;
  cursor: pointer;
}
.od-dot[aria-current="true"] { background: #2266aa; }
.od-pause {
  border: 0;
  background: transparent;
  color: #555;
  font-size: 12px;
  cursor: pointer;
}
.od-carousel button:focus-visible,
.od-project-link:focus-visible {
  outline: 3px solid #2266aa;
  outline-offset: -3px;
}
@media (max-width: 600px) {
  .od-caption { padding: 14px 20px 8px; }
  .od-caption p { font-size: 13px; }
}
.od-arrow {
  display: none;
}
</style>

<div class="od-carousel" id="od-carousel"
     role="region" aria-roledescription="carousel"
     aria-label="Selected research projects" markdown="0">

  <a class="od-project-link" id="od-project-link"
     href="https://yijionglin.github.io/tactilelab/"
     target="_blank" rel="noopener noreferrer">
    <div class="od-media">
      <img id="od-project-image"
           class="is-visible"
           src="{{ '/images/projects/tactilelab_1.gif' | relative_url }}"
           alt="TactileLab project demonstration">
      <img id="od-project-image-next" alt="" aria-hidden="true">
    </div>
    <div class="od-caption">
      <h3 id="od-project-title">TactileLab</h3>
      <p id="od-project-description">
        Multimodal tactile simulation for dexterous sim-to-real manipulation.
      </p>
      <span class="od-visit">Visit project website ↗</span>
    </div>
  </a>

  <button class="od-arrow od-prev" type="button"
          aria-label="Previous project">‹</button>
  <button class="od-arrow od-next" type="button"
          aria-label="Next project">›</button>

  <div class="od-controls">
    <div id="od-dots" style="display:flex;gap:10px"></div>
    <button class="od-pause" id="od-pause" type="button">
      Pause slideshow
    </button>
  </div>
</div>

<script>
(function () {
  const projects = [
    {
      title: "TactileLab: Efficient Multimodal Tactile Simulation for Shear-Sensitive Dexterous Sim2Real Robotic Manipulation",
      image: "{{ '/images/projects/tactilelab_1.gif' | relative_url }}",
      url: "https://yijionglin.github.io/tactilelab/",
      // description: "Efficient Multimodal Tactile Simulation for Shear-Sensitive Dexterous Sim2Real Robotic Manipulation."
    },
    {
      title: "TactileLab: Efficient Multimodal Tactile Simulation for Shear-Sensitive Dexterous Sim2Real Robotic Manipulation",
      image: "{{ '/images/projects/tactilelab_2.gif' | relative_url }}",
      url: "https://yijionglin.github.io/tactilelab/",
    },
    {
      title: "TactileLab: Efficient Multimodal Tactile Simulation for Shear-Sensitive Dexterous Sim2Real Robotic Manipulation",
      image: "{{ '/images/projects/tactilelab_3.gif' | relative_url }}",
      url: "https://yijionglin.github.io/tactilelab/",
    },

    {
      title: "NeuralTouch: Neural Descriptors for Precise Sim-to-Real Tactile Robot Control",
      image: "{{ '/images/projects/neuraltouch.gif' | relative_url }}",
      url: "https://yijionglin.github.io/neuraltouch/",
    },
    {
      title: "Bi-Touch: Bimanual Tactile Manipulation With Sim-to-Real Deep Reinforcement Learning",
      image: "{{ '/images/projects/bitouch.gif' | relative_url }}",
      url: "https://sites.google.com/view/bi-touch/",
    },
    {
      title: "SimShear: Sim-to-Real Shear-based Tactile Servoing",
      image: "{{ '/images/projects/simshear.gif' | relative_url }}",
      url: "https://yijionglin.github.io/simshear/",
    },
    {
      title: "AnyRotate: Gravity-Invariant In-Hand Object Rotation with Sim-to-Real Touch",
      image: "{{ '/images/projects/anyrotate.gif' | relative_url }}",
      url: "https://maxyang27896.github.io/anyrotate/",
    }
  ];

  const root = document.getElementById("od-carousel");
  const img = document.getElementById("od-project-image");
  const nextImg = document.getElementById("od-project-image-next");
  const images = [img, nextImg];
  const link = document.getElementById("od-project-link");
  const title = document.getElementById("od-project-title");
  const description = document.getElementById("od-project-description");
  const dots = document.getElementById("od-dots");
  const pause = document.getElementById("od-pause");

  let index = 0;
  let activeImageIndex = 0;
  let timer;
  let transitionTimer;
  let transitionToken = 0;
  let transitioning = false;
  let focused = false;
  let paused = window.matchMedia("(prefers-reduced-motion: reduce)").matches;

  function schedule() {
    clearTimeout(timer);
    if (!paused && !focused && !document.hidden &&
        !transitioning && images[activeImageIndex].complete) {
      timer = setTimeout(function () { show(index + 1); }, 3000);
    }
  }

  function show(next) {
    clearTimeout(timer);
    clearTimeout(transitionTimer);
    index = (next + projects.length) % projects.length;
    const project = projects[index];

    link.href = project.url;
    title.textContent = project.title;
    description.textContent = project.description;

    Array.from(dots.children).forEach(function (dot, i) {
      dot.setAttribute("aria-current", String(i === index));
    });

    const outgoing = images[activeImageIndex];
    if (outgoing.getAttribute("src") === project.image) {
      transitioning = false;
      schedule();
      return;
    }

    const incomingIndex = 1 - activeImageIndex;
    const incoming = images[incomingIndex];
    const token = ++transitionToken;
    let transitionStarted = false;
    transitioning = true;
    incoming.alt = project.title + " project demonstration";

    function beginTransition() {
      if (token !== transitionToken || transitionStarted) return;
      transitionStarted = true;
      incoming.classList.add("is-visible");
      incoming.removeAttribute("aria-hidden");
      outgoing.classList.remove("is-visible");
      outgoing.setAttribute("aria-hidden", "true");
      activeImageIndex = incomingIndex;
      transitionTimer = setTimeout(function () {
        transitioning = false;
        schedule();
      }, 500);
    }

    incoming.onload = beginTransition;
    incoming.onerror = function () {
      if (token !== transitionToken) return;
      console.error("Unable to load project image: " + project.image);
      transitioning = false;
      schedule();
    };
    incoming.src = project.image;
    if (incoming.complete && incoming.naturalWidth > 0) beginTransition();

    schedule();
  }

  projects.forEach(function (project, i) {
    const dot = document.createElement("button");
    dot.type = "button";
    dot.className = "od-dot";
    dot.setAttribute("aria-label", "Show " + project.title);
    dot.addEventListener("click", function () { show(i); });
    dots.appendChild(dot);
  });

  root.querySelector(".od-prev").onclick = function () { show(index - 1); };
  root.querySelector(".od-next").onclick = function () { show(index + 1); };

  function updatePause() {
    pause.textContent = paused ? "Play slideshow" : "Pause slideshow";
  }

  pause.onclick = function () {
    paused = !paused;
    updatePause();
    schedule();
  };

  root.addEventListener("focusin", function () {
    focused = true;
    schedule();
  });
  root.addEventListener("focusout", function (event) {
    focused = root.contains(event.relatedTarget);
    schedule();
  });

  let startX = 0;
  let startY = 0;
  let swiped = false;

  link.addEventListener("touchstart", function (event) {
    startX = event.changedTouches[0].clientX;
    startY = event.changedTouches[0].clientY;
    swiped = false;
  }, { passive: true });

  link.addEventListener("touchend", function (event) {
    const dx = event.changedTouches[0].clientX - startX;
    const dy = event.changedTouches[0].clientY - startY;
    if (Math.abs(dx) > 50 && Math.abs(dx) > Math.abs(dy)) {
      swiped = true;
      show(index + (dx < 0 ? 1 : -1));
    }
  }, { passive: true });

  link.addEventListener("click", function (event) {
    if (swiped) {
      event.preventDefault();
      swiped = false;
    }
  });

  img.addEventListener("load", schedule);
  img.addEventListener("error", schedule);
  document.addEventListener("visibilitychange", schedule);

  updatePause();
  show(0);
})();

</script>



We develop robots that learn to perceive and interact with the physical
world through touch. Our research combines tactile sensing, multimodal
perception, and robot learning to enable dexterous manipulation in complex,
contact-rich environments.

We focus on three closely connected research directions:

- **Tactile sensing and perception:** Understanding contact, geometry,
  and motion through vision-based tactile sensors and multimodal
  representations.

- **Simulation and robot learning:** Building scalable tactile
  simulation and sim-to-real learning methods that transfer robot
  skills from virtual environments to the real world.

- **Dexterous robotic manipulation:** Developing touch-guided skills
  for in-hand manipulation, bimanual coordination, and precise
  contact-rich tasks.
