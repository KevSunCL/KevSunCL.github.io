---
permalink: /
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
/* ── Hero banner ── */
.hero-banner {
  background: linear-gradient(135deg, #e0f2fe 0%, #bae6fd 40%, #7dd3fc 100%);
  color: #0c4a6e;
  padding: 2rem 2rem;
  border-radius: 10px;
  margin-bottom: 2rem;
  position: relative;
  overflow: hidden;
  border: 1px solid #7dd3fc;
}
.hero-banner::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -20%;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(255,255,255,0.5) 0%, transparent 70%);
  border-radius: 50%;
}
.hero-banner h2 {
  margin: 0 0 0.3rem 0;
  font-size: 1.4rem;
  color: #0c4a6e;
  font-weight: 700;
  letter-spacing: 0.5px;
}
.hero-banner .hero-subtitle {
  font-size: 1.05rem;
  color: #075985;
  margin-bottom: 0.2rem;
  font-weight: 500;
}
.hero-banner .hero-affiliation {
  font-size: 0.92rem;
  color: #0369a1;
}

/* ── Stats row ── */
.stats-row {
  display: flex;
  gap: 1rem;
  margin: 1.5rem 0 2rem 0;
  flex-wrap: wrap;
}
.stat-card {
  flex: 1;
  min-width: 140px;
  background: #f7f9fc;
  border: 1px solid #e2e8f0;
  border-left: 4px solid #2c5282;
  border-radius: 6px;
  padding: 1rem 1.1rem;
  text-align: center;
  transition: transform 0.2s, box-shadow 0.2s;
}
.stat-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(44,82,130,0.12);
}
.stat-card .stat-number {
  font-size: 1.6rem;
  font-weight: 800;
  color: #2c5282;
  line-height: 1.2;
}
.stat-card .stat-label {
  font-size: 0.78rem;
  color: #5a6a7e;
  margin-top: 0.25rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

/* ── Research cards ── */
.research-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 1rem;
  margin: 1.2rem 0 2rem 0;
}
@media (max-width: 900px) {
  .research-grid { grid-template-columns: 1fr 1fr; }
}
@media (max-width: 700px) {
  .research-grid { grid-template-columns: 1fr; }
}
.research-card {
  background: #fff;
  border: 1px solid #e2e8f0;
  border-radius: 8px;
  padding: 1.2rem 1.3rem;
  transition: transform 0.2s, box-shadow 0.2s;
}
.research-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 18px rgba(0,0,0,0.08);
}
.research-card .card-icon {
  font-size: 1.6rem;
  margin-bottom: 0.4rem;
}
.research-card h4 {
  margin: 0 0 0.4rem 0;
  font-size: 0.95rem;
  color: #1a365d;
}
.research-card p {
  margin: 0;
  font-size: 0.85rem;
  color: #4a5568;
  line-height: 1.5;
}

/* ── Timeline ── */
.timeline {
  position: relative;
  padding-left: 28px;
  margin: 1rem 0 2rem 0;
}
.timeline::before {
  content: '';
  position: absolute;
  left: 8px;
  top: 4px;
  bottom: 4px;
  width: 2px;
  background: linear-gradient(to bottom, #2c5282, #93b5e1);
}
.timeline-item {
  position: relative;
  margin-bottom: 1.1rem;
}
.timeline-item::before {
  content: '';
  position: absolute;
  left: -24px;
  top: 6px;
  width: 12px;
  height: 12px;
  border-radius: 50%;
  background: #2c5282;
  border: 2px solid #fff;
  box-shadow: 0 0 0 2px #2c5282;
}
.timeline-item.current::before {
  background: #38a169;
  box-shadow: 0 0 0 2px #38a169;
}
.timeline-item .tl-title {
  font-weight: 700;
  font-size: 0.92rem;
  color: #1a202c;
}
.timeline-item .tl-detail {
  font-size: 0.84rem;
  color: #5a6a7e;
}

/* ── Editorial badges ── */
.badge-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  margin: 0.8rem 0 1.5rem 0;
}
.badge {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  background: #edf2f7;
  border: 1px solid #cbd5e0;
  border-radius: 20px;
  padding: 0.4rem 0.9rem;
  font-size: 0.82rem;
  color: #2d3748;
  font-weight: 500;
  transition: background 0.2s;
}
.badge:hover { background: #e2e8f0; }
.badge .badge-dot {
  width: 7px; height: 7px;
  border-radius: 50%;
  background: #2c5282;
  flex-shrink: 0;
}

/* ── Skills bars ── */
.skills-section {
  margin: 1rem 0 2rem 0;
}
.skill-item {
  margin-bottom: 0.7rem;
}
.skill-item .skill-header {
  display: flex;
  justify-content: space-between;
  font-size: 0.84rem;
  margin-bottom: 0.25rem;
  color: #2d3748;
  font-weight: 600;
}
.skill-bar {
  height: 8px;
  background: #e2e8f0;
  border-radius: 4px;
  overflow: hidden;
}
.skill-fill {
  height: 100%;
  border-radius: 4px;
  background: linear-gradient(90deg, #2c5282, #4299e1);
}

/* ── Section title accent ── */
.section-title {
  font-size: 1.15rem;
  color: #1a365d;
  border-bottom: 2px solid #2c5282;
  padding-bottom: 0.4rem;
  margin: 2rem 0 1rem 0;
  display: inline-block;
}

/* ── CTA box ── */
.cta-box {
  background: linear-gradient(135deg, #ebf4ff 0%, #f0f7ff 100%);
  border: 1px solid #bee3f8;
  border-radius: 8px;
  padding: 1.3rem 1.5rem;
  margin-top: 2rem;
  text-align: center;
}
.cta-box p {
  margin: 0;
  font-size: 0.92rem;
  color: #2d3748;
  line-height: 1.6;
  font-style: italic;
}
</style>

<!-- ═══════════ HERO BANNER ═══════════ -->
<div class="hero-banner">
  <h2>Kevin (Kun) Sun 孙坤</h2>
  <div class="hero-subtitle">Full Tenured Professor of Computational Linguistics</div>
  <div class="hero-affiliation">Director, Institute of AI and Language Science · School of Foreign Languages, Tongji University</div>
</div>

I am the **Director of the Institute of AI and Language Science** and a **Full Tenured Professor of Computational Linguistics** at Tongji University. My research investigates **how language and contextual meaning are represented and processed in human and artificial intelligence**, bridging computational linguistics, cognitive science, and AI.

My work centers on three interconnected areas: **computational language and human cognition**, **language intelligence in AI**, and **human–AI cognitive alignment**. I combine computational modeling and large language models with behavioral and cognitive-neuroscience methods, including eye-tracking, EEG, and fMRI, to study language comprehension and representation across humans and machines. A particular focus is the development of **interpretable computational measures** that connect linguistic structure and context with machine representations and human behavioral and neural dynamics.

More broadly, I aim to develop a **cognitively grounded science of language and AI** that uses insights from human language and cognition to understand, evaluate, and improve artificial intelligence.

<!-- ═══════════ STATS AT A GLANCE ═══════════ -->
<div class="stats-row">
  <div class="stat-card">
    <div class="stat-number">60+</div>
    <div class="stat-label">International Journal Publications</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">6+</div>
    <div class="stat-label">Programming Languages</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">4</div>
    <div class="stat-label">Editorial Board Roles</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">4</div>
    <div class="stat-label">Languages</div>
  </div>
</div>

<!-- ═══════════ RESEARCH FOCUS ═══════════ -->
<h2 class="section-title">🔬 Research Focus</h2>

My research investigates **how language and contextual meaning are represented and processed in human and artificial intelligence**. It spans three core themes—**computational language and human cognition**, **language intelligence in AI**, and **human–AI cognitive alignment**—with complementary work in speech, computational discourse, and responsible AI.

<div class="research-grid">

  <div class="research-card">
    <div class="card-icon">🧠</div>
    <h4>Computational Language & Human Cognition</h4>
    <p>
      Developing interpretable computational models of language comprehension,
      prediction, semantic integration, and discourse processing, using behavioral,
      eye-tracking, EEG, and fMRI evidence.
    </p>
  </div>

  <div class="research-card">
    <div class="card-icon">🤖</div>
    <h4>Language Intelligence in AI</h4>
    <p>
      Investigating the linguistic, pragmatic, and reasoning capabilities of large
      language models, including their internal representations, contextual
      generalization, and mechanisms of language understanding.
    </p>
  </div>

  <div class="research-card">
    <div class="card-icon">🔗</div>
    <h4>Human–AI Cognitive Alignment</h4>
    <p>
      Comparing human behavioral and neural dynamics with representations and
      computations in artificial models to identify where human and machine
      language processing converge and diverge.
    </p>
  </div>

  <div class="research-card">
    <div class="card-icon">🎙️</div>
    <h4>Speech & Multimodal Language Processing</h4>
    <p>
      Studying spoken-language processing through computational modeling,
      self-supervised speech representations, prosody, and multimodal signals,
      with a focus on links between linguistic structure and human cognition.
    </p>
  </div>

  <div class="research-card">
    <div class="card-icon">📜</div>
    <h4>Computational Discourse & Digital Humanities</h4>
    <p>
      Developing computational approaches to discourse structure, coherence,
      information flow, language change, and large-scale text analysis across
      languages, genres, and historical corpora.
    </p>
  </div>

  <div class="research-card">
    <div class="card-icon">⚖️</div>
    <h4>Responsible AI, Evaluation & Language Education</h4>
    <p>
      Evaluating AI systems for linguistic competence, cognitive and cultural
      biases, and human alignment, while translating computational language
      research into responsible applications in language education and digital
      scholarship.
    </p>
  </div>

</div>

<!-- ═══════════ CAREER TIMELINE ═══════════ -->
<h2 class="section-title">🎓 Academic Positions</h2>

<div class="timeline">
  <div class="timeline-item current">
    <div class="tl-title">Full Tenured Professor & Institute Director</div>
    <div class="tl-detail">Tongji University · Institute of AI and Language Science · 2025–present</div>
  </div>
  <div class="timeline-item">
    <div class="tl-title">Habilitation (German Professorship Qualification)</div>
    <div class="tl-detail">University of Tübingen · 2024</div>
  </div>
  <div class="timeline-item">
    <div class="tl-title">Assistant Professor & Research Scientist</div>
    <div class="tl-detail">University of Tübingen · 2017–2025</div>
  </div>
</div>

<!-- ═══════════ JOURNAL EDITORIAL ROLES ═══════════ -->
<h2 class="section-title">📝 Journal Editorial Roles</h2>

<div class="badge-row">
  <span class="badge"><span class="badge-dot"></span>Review Editor · Frontiers in Psychology</span>
  <span class="badge"><span class="badge-dot"></span>Editorial Board · Scientific Reports （journal published by Nature）</span>
   <span class="badge"><span class="badge-dot"></span>Editorial Board · Humanites and Social Communications (journal published by Nature)</span>
  <span class="badge"><span class="badge-dot"></span>Editorial Board · BMC Psychology</span>
</div>

<!-- ═══════════ IMPACT & RECOGNITION ═══════════ -->
<h2 class="section-title">🏆 Impact & Recognition</h2>

My research has led to **30+ peer-reviewed journal publications** in top-tier international venues including *Cognition*, *Cognitive Science*, *Linguistics*, *Neural Networks*, and *PNAS*, and **10  confernce papers** in ACL and other AI top conferences, as well as **10+ publications** in leading Chinese CSSCI journals such as *中国语文* and *当代语言学*. Many of my works have been reprinted in *人大复印资料* and *中国社会科学文摘*. My research has been featured in **MIT Technology Review**.

<!-- ═══════════ TECHNICAL EXPERTISE ═══════════ -->
<h2 class="section-title">💻 Technical Expertise</h2>

<div class="skills-section">
  <div class="skill-item">
    <div class="skill-header"><span>Python</span><span>Advanced</span></div>
    <div class="skill-bar"><div class="skill-fill" style="width: 95%"></div></div>
  </div>
  <div class="skill-item">
    <div class="skill-header"><span>R</span><span>Advanced</span></div>
    <div class="skill-bar"><div class="skill-fill" style="width: 92%"></div></div>
  </div>
  <div class="skill-item">
    <div class="skill-header"><span>PyTorch</span><span>Advanced</span></div>
    <div class="skill-bar"><div class="skill-fill" style="width: 90%"></div></div>
  </div>
  <div class="skill-item">
    <div class="skill-header"><span>C</span><span>Intermediate</span></div>
    <div class="skill-bar"><div class="skill-fill" style="width: 60%"></div></div>
  </div>
  <div class="skill-item">
    <div class="skill-header"><span>Linux Shell</span><span>Intermediate</span></div>
    <div class="skill-bar"><div class="skill-fill" style="width: 60%"></div></div>
  </div>
</div>

**Experimental Methods**: Eye-tracking · EEG · fMRI · Online experiments  
**Languages**: Chinese (native) · English (fluent) · German (intermediate) · Japanese (intermediate)

<!-- ═══════════ CURRENT PROJECTS ═══════════ -->
<h2 class="section-title">🚀 Current Projects</h2>

My current projects examine **language and contextual meaning across human and artificial intelligence**, connecting computational modeling, cognitive neuroscience, large language models, and speech technologies:

- **Contextual meaning in human language comprehension:** investigating how semantic relevance, contextual fit, and surprisal independently shape reading, speech processing, and neural dynamics using behavioral, eye-tracking, EEG, and fMRI data

- **Language intelligence and internal representations in LLMs:** studying reasoning, pragmatics, contextual generalization, and internal representations through controlled evaluation, probing, and representation-level analysis

- **Human–AI cognitive alignment:** comparing human behavioral and neural responses with computational measures and model representations to identify shared and divergent mechanisms of language processing

- **Speech representations and linguistic structure:** investigating how speech self-supervised learning models encode linguistic information, including the sparse localization and representation of various linguistic expressions

- **Affective and social language intelligence:** examining how humans and language models represent emotion, figurative meaning, politeness, and other socially situated aspects of language across languages and contexts.

<!-- ═══════════ CONTACT CTA ═══════════ -->
<div class="cta-box">
  <p>I'm always excited to discuss research collaborations, student supervision opportunities, or innovative applications of computational linguistics, AI and cognitive computation. Feel free to reach out at <b>sharpksun at hotmail.com</b>!</p>
</div>
