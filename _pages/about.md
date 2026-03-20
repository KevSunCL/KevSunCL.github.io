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
  background: linear-gradient(135deg, #1a1a2e 0%, #16213e 40%, #0f3460 100%);
  color: #e8e8e8;
  padding: 2rem 2rem;
  border-radius: 10px;
  margin-bottom: 2rem;
  position: relative;
  overflow: hidden;
}
.hero-banner::before {
  content: '';
  position: absolute;
  top: -50%;
  right: -20%;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(83,144,217,0.15) 0%, transparent 70%);
  border-radius: 50%;
}
.hero-banner h2 {
  margin: 0 0 0.3rem 0;
  font-size: 1.4rem;
  color: #fff;
  font-weight: 700;
  letter-spacing: 0.5px;
}
.hero-banner .hero-subtitle {
  font-size: 1.05rem;
  color: #93b5e1;
  margin-bottom: 0.2rem;
  font-weight: 500;
}
.hero-banner .hero-affiliation {
  font-size: 0.92rem;
  color: #a8bdd4;
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

I am the **Director of the Institute of AI and Language Science** and a **Full Tenured Professor of Computational Linguistics** in the School of Foreign Languages at Tongji University. I explore the fascinating intersection of **computational linguistics**, **cognitive computation**, and **artificial intelligence**. My research bridges the gap between human language processing and machine learning, integrating statistical modeling, deep learning, and cognitive-neuroscience experimental methods to understand the deep mechanisms of language understanding and processing in both humans and machines. I have developed a number of specialized large language models, as well as major databases and corpora, widely used in academia and industry. As global efforts accelerate in "AI + Education", I am committed to applying data-driven approaches to advance language research toward big language science.

<!-- ═══════════ STATS AT A GLANCE ═══════════ -->
<div class="stats-row">
  <div class="stat-card">
    <div class="stat-number">30+</div>
    <div class="stat-label">International Journal Publications</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">10+</div>
    <div class="stat-label">Chinese CSSCI Publications</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">3</div>
    <div class="stat-label">Editorial Board Roles</div>
  </div>
  <div class="stat-card">
    <div class="stat-number">4</div>
    <div class="stat-label">Languages</div>
  </div>
</div>

<!-- ═══════════ RESEARCH FOCUS ═══════════ -->
<h2 class="section-title">🔬 Research Focus</h2>

My work sits at the cutting edge of **computational linguistics** and **cognitive AI**, where I develop novel computational methods to understand human language processing and machine intelligence.

<div class="research-grid">
  <div class="research-card">
    <div class="card-icon">🧠</div>
    <h4>Cognitive Computation & Brain-inspired AI</h4>
    <p>Developing computational models that explain how humans process language, using eye-tracking, EEG, and fMRI data to understand the neural mechanisms of discourse comprehension.</p>
  </div>
  <div class="research-card">
    <div class="card-icon">🤖</div>
    <h4>Large Language Models & Reasoning</h4>
    <p>Evaluating and enhancing LLM reasoning capabilities, fine-tuning transformer-based models, and developing attention-aware computational metrics for multi-modal language processing.</p>
  </div>
  <div class="research-card">
    <div class="card-icon">💭</div>
    <h4>Affective Computing</h4>
    <p>Understanding emotion and sentiment in human language through computational approaches, bridging cognitive and affective dimensions of language.</p>
  </div>
  <div class="research-card">
    <div class="card-icon">📊</div>
    <h4>Advanced Statistical Analysis</h4>
    <p>Applying sophisticated statistical methods including GAMM, Bayesian modeling, and time-series analysis to linguistic and cognitive phenomena.</p>
  </div>
  <div class="research-card">
    <div class="card-icon">📜</div>
    <h4>Digital Humanities & Computational Text Analysis</h4>
    <p>Formal and computational models of discourse structure; computational measurement of coherence, cohesion, and information flow; graph-based and network representations of discourse; discourse dependency and cross-framework conversion (RST, PDTB, dependency); multilingual discourse parsing; distant reading and large-scale diachronic analysis of literary and scholarly texts; computational modeling of lexical semantic change and language evolution.</p>
  </div>
  <div class="research-card">
    <div class="card-icon">⚖️</div>
    <h4>AI Methods, Ethics & Didactics</h4>
    <p>Efficient training and inference in LLMs; evaluations and benchmarking of AI models; cognitive-inspired reasoning in LLMs; critical assessment of AI biases, cultural tendencies, and societal impacts; development of DH-related curricula integrating AI literacy and ethical reflection.</p>
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
  <span class="badge"><span class="badge-dot"></span>Editorial Board · Scientific Reports</span>
  <span class="badge"><span class="badge-dot"></span>Editorial Board · BMC Psychology</span>
</div>

<!-- ═══════════ IMPACT & RECOGNITION ═══════════ -->
<h2 class="section-title">🏆 Impact & Recognition</h2>

My research has led to **30+ peer-reviewed journal publications** in top-tier international venues including *Cognition*, *Cognitive Science*, *Linguistics*, *Neural Networks*, and *PNAS*, as well as **10+ publications** in leading Chinese CSSCI journals such as *中国语文* and *当代语言学*. Many of my works have been reprinted in *人大复印资料* and *中国社会科学文摘*. My research has been featured in **MIT Technology Review**.

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

I'm currently working on groundbreaking projects that combine **cognitive neuroscience** with **artificial intelligence** to understand how humans and machines process language:

- Large Language Model reasoning and evaluation frameworks
- Cognitive computation models for brain-inspired AI
- Advanced statistical approaches to linguistic and cognitive data using GAMM and Bayesian methods
- Cross-linguistic and multi-modal studies of affective computing

<!-- ═══════════ CONTACT CTA ═══════════ -->
<div class="cta-box">
  <p>I'm always excited to discuss research collaborations, student supervision opportunities, or innovative applications of computational linguistics, AI and cognitive computation. Feel free to reach out at <b>sharpksun at hotmail.com</b>!</p>
</div>
