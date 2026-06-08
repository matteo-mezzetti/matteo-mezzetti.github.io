---
layout: default
title: Projects
---

<div class="page-header">
  <h1>Projects</h1>
  <p>Things I've built, broken, and fixed.</p>
</div>

<div class="carousel-wrap">
  <div class="carousel">

    <div class="card" onclick="openModal(0)">
      <div class="card-img" style="background: linear-gradient(135deg, #1a0000 0%, #3d0000 100%);"></div>
      <div class="card-body">
        <div class="card-title">Unified Team Intranet</div>
        <div class="card-desc">Centralised Google Workspace intranet replacing 6 siloed team drives for a 100+ person student org.</div>
        <div class="card-tags">
          <span class="card-tag">Google Workspace</span>
          <span class="card-tag">Sites</span>
          <span class="card-tag">Drive</span>
        </div>
      </div>
    </div>

    <div class="card" onclick="openModal(1)">
      <div class="card-img" style="background: linear-gradient(135deg, #001a1f 0%, #003d4d 100%);"></div>
      <div class="card-body">
        <div class="card-title">(WIP) Prediction Song Hotness in the Million Song Dataset</div>
        <div class="card-desc">Just wait and see what I cook up...</div>
        <div class="card-tags">
          <span class="card-tag">R</span>
          <span class="card-tag">SQL</span>
          <span class="card-tag">ggplot2</span>
        </div>
      </div>
    </div>

    <div class="card" onclick="openModal(2)">
      <div class="card-img" style="background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);"></div>
      <div class="card-body">
        <div class="card-title">(WIP) Vineyard Management Database</div>
        <div class="card-desc">Watch this space and see what I cook up...</div>
        <div class="card-tags">
          <span class="card-tag">Python</span>
          <span class="card-tag">pandas</span>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- Modal overlay -->
<div class="modal-bg" id="modalBg" onclick="closeModalBg(event)">
  <div class="modal-wrap">
    <div class="modal" id="modal">
      <div class="modal-img" id="modalImg"></div>
      <div class="modal-body">
        <div class="modal-title" id="modalTitle"></div>
        <div class="modal-desc" id="modalDesc"></div>
        <div class="modal-tags" id="modalTags"></div>
        <a href="#" class="modal-link" id="modalLink">View on GitHub →</a>
      </div>
    </div>
    <button class="modal-close" onclick="document.getElementById('modalBg').classList.remove('open')">✕</button>
  </div>
</div>

<script>
var projects = [
  {
    title: "(WIP) Unified Team Intranet",
    desc: "Centralised Google Workspace intranet replacing 6 siloed team drives for a 100+ person student organisation. Includes a shared calendar, document library, and onboarding flow.",
    tags: ["Google Workspace"],
    bg: "linear-gradient(135deg, #1a0000 0%, #3d0000 100%)",
    link: "#"
  },
  {
    title: "(WIP) Prediction Song Hotness in the Million Song Dataset",
    desc: "Watch this space and see what I cook up...",
    tags: ["R", "ggplot2"],
    bg: "linear-gradient(135deg, #001a1f 0%, #003d4d 100%)",
    link: "#"
  },
  {
    title: "(WIP) Vineyard Management Database",
    desc: "Watch this space and see what I cook up...",
    tags: ["MySQL"],
    bg: "linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%)",
    link: "#"
  }
  
  
];

function openModal(i) {
  var p = projects[i];
  document.getElementById('modalTitle').textContent = p.title;
  document.getElementById('modalDesc').textContent = p.desc;
  document.getElementById('modalImg').style.background = p.bg;
  document.getElementById('modalLink').href = p.link;
  var tags = document.getElementById('modalTags');
  tags.innerHTML = p.tags.map(function(t){ return '<span class="modal-tag">' + t + '</span>'; }).join('');
  document.getElementById('modalBg').classList.add('open');
}

function closeModalBg(e) {
  if (e.target === document.getElementById('modalBg')) {
    document.getElementById('modalBg').classList.remove('open');
  }
}

document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') document.getElementById('modalBg').classList.remove('open');
});
</script>
