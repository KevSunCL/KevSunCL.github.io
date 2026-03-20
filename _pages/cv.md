---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<style>
/* ── CV Hero — darker, tech-inspired ── */
.cv-hero {
  background: linear-gradient(160deg, #064e3b 0%, #065f46 40%, #047857 70%, #059669 100%);
  color: #d1fae5;
  padding: 2.2rem 2rem;
  border-radius: 8px;
  margin-bottom: 2rem;
  position: relative;
  overflow: hidden;
  border: 1px solid #10b981;
}
.cv-hero::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0; bottom: 0;
  background: repeating-linear-gradient(
    0deg,
    transparent,
    transparent 40px,
    rgba(16,185,129,0.1) 40px,
    rgba(16,185,129,0.1) 41px
  );
  pointer-events: none;
}
.cv-hero::after {
  content: '';
  position: absolute;
  top: -40%;
  right: -15%;
  width: 380px;
  height: 380px;
  background: radial-gradient(circle, rgba(52,211,153,0.15) 0%, transparent 70%);
  border-radius: 50%;
  pointer-events: none;
}
.cv-hero .cv-name {
  font-size: 1.5rem;
  font-weight: 800;
  color: #ffffff;
  letter-spacing: 1px;
  margin-bottom: 0.3rem;
  position: relative;
}
.cv-hero .cv-title {
  font-size: 1rem;
  color: #6ee7b7;
  font-weight: 500;
  margin-bottom: 0.15rem;
  position: relative;
}
.cv-hero .cv-affil {
  font-size: 0.88rem;
  color: #a7f3d0;
  position: relative;
}
.cv-hero .cv-contact {
  margin-top: 0.8rem;
  position: relative;
  font-size: 0.82rem;
  color: #a7f3d0;
}
.cv-hero .cv-contact a {
  color: #6ee7b7;
  text-decoration: none;
}
.cv-hero .cv-contact a:hover {
  text-decoration: underline;
}

/* ── Section header — left accent bar ── */
.cv-section {
  font-size: 1.05rem;
  font-weight: 700;
  color: #1a1a2e;
  padding: 0.5rem 0 0.5rem 1rem;
  margin: 2.2rem 0 1rem 0;
  border-left: 4px solid #059669;
  background: linear-gradient(90deg, #ecfdf5 0%, transparent 100%);
  letter-spacing: 0.3px;
}

/* ── Timeline — compact, elegant ── */
.cv-timeline {
  position: relative;
  padding-left: 24px;
  margin: 0.8rem 0 1.5rem 0;
}
.cv-timeline::before {
  content: '';
  position: absolute;
  left: 6px;
  top: 6px;
  bottom: 6px;
  width: 1.5px;
  background: #d0d7de;
}
.cv-tl-item {
  position: relative;
  margin-bottom: 1rem;
  padding-bottom: 0.2rem;
}
.cv-tl-item::before {
  content: '';
  position: absolute;
  left: -21px;
  top: 7px;
  width: 9px;
  height: 9px;
  border-radius: 50%;
  background: #065f46;
  border: 2px solid #fff;
  box-shadow: 0 0 0 1.5px #065f46;
}
.cv-tl-item.active::before {
  background: #1f883d;
  box-shadow: 0 0 0 1.5px #1f883d;
}
.cv-tl-item .tl-role {
  font-weight: 700;
  font-size: 0.9rem;
  color: #1a1a2e;
}
.cv-tl-item .tl-org {
  font-size: 0.84rem;
  color: #57606a;
}
.cv-tl-item .tl-date {
  display: inline-block;
  font-size: 0.72rem;
  font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
  color: #656d76;
  background: #f6f8fa;
  border: 1px solid #d0d7de;
  border-radius: 12px;
  padding: 0.1rem 0.5rem;
  margin-top: 0.15rem;
}

/* ── Stat pills ── */
.cv-stats {
  display: flex;
  gap: 0.7rem;
  margin: 1rem 0 1.5rem 0;
  flex-wrap: wrap;
}
.cv-pill {
  flex: 1;
  min-width: 110px;
  background: #f6f8fa;
  border: 1px solid #d0d7de;
  border-radius: 6px;
  padding: 0.8rem 0.9rem;
  text-align: center;
  transition: border-color 0.2s;
}
.cv-pill:hover {
  border-color: #059669;
}
.cv-pill .pill-num {
  font-size: 1.4rem;
  font-weight: 800;
  color: #065f46;
  line-height: 1.2;
  font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
}
.cv-pill .pill-lbl {
  font-size: 0.7rem;
  color: #57606a;
  margin-top: 0.15rem;
  text-transform: uppercase;
  letter-spacing: 0.4px;
}

/* ── Research interest chips ── */
.ri-group {
  margin-bottom: 1rem;
}
.ri-group .ri-title {
  font-weight: 700;
  font-size: 0.88rem;
  color: #065f46;
  margin-bottom: 0.3rem;
}
.ri-group .ri-desc {
  font-size: 0.83rem;
  color: #57606a;
  line-height: 1.55;
  padding-left: 0.8rem;
  border-left: 2px solid #d0d7de;
}

/* ── Compact list card ── */
.cv-card {
  background: #fff;
  border: 1px solid #d0d7de;
  border-radius: 6px;
  padding: 1rem 1.2rem;
  margin-bottom: 0.8rem;
  transition: border-color 0.2s;
}
.cv-card:hover {
  border-color: #065f46;
}
.cv-card h4 {
  margin: 0 0 0.3rem 0;
  font-size: 0.9rem;
  color: #065f46;
}
.cv-card p, .cv-card li {
  font-size: 0.84rem;
  color: #57606a;
  line-height: 1.55;
}
.cv-card ul {
  margin: 0.3rem 0 0 0;
  padding-left: 1.2rem;
}
.cv-card li {
  margin-bottom: 0.2rem;
}

/* ── Tag badges ── */
.cv-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  margin: 0.5rem 0;
}
.cv-tag {
  display: inline-block;
  font-size: 0.75rem;
  font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
  background: #f6f8fa;
  border: 1px solid #d0d7de;
  border-radius: 4px;
  padding: 0.2rem 0.55rem;
  color: #065f46;
  font-weight: 500;
}
.cv-tag-green {
  background: #dafbe1;
  border-color: #82e596;
  color: #116329;
}
.cv-tag-blue {
  background: #ddf4ff;
  border-color: #80ccff;
  color: #0550ae;
}
.cv-tag-purple {
  background: #eddeff;
  border-color: #c297ff;
  color: #5b21b6;
}
.cv-tag-amber {
  background: #fff8c5;
  border-color: #f5c543;
  color: #6f4e00;
}

/* ── Award items ── */
.award-item {
  display: flex;
  align-items: flex-start;
  gap: 0.6rem;
  padding: 0.5rem 0;
  border-bottom: 1px solid #f0f0f0;
  font-size: 0.85rem;
}
.award-item:last-child { border-bottom: none; }
.award-item .aw-year {
  font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
  font-size: 0.76rem;
  color: #656d76;
  background: #f6f8fa;
  border: 1px solid #d0d7de;
  border-radius: 4px;
  padding: 0.15rem 0.4rem;
  white-space: nowrap;
  flex-shrink: 0;
}
.award-item .aw-text {
  color: #1a1a2e;
}

/* ── Funding table ── */
.fund-item {
  background: #fff;
  border: 1px solid #d0d7de;
  border-radius: 6px;
  padding: 0.8rem 1rem;
  margin-bottom: 0.6rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 0.5rem;
  transition: border-color 0.2s;
}
.fund-item:hover { border-color: #065f46; }
.fund-item .fund-name {
  font-size: 0.85rem;
  color: #065f46;
  font-weight: 600;
  flex: 1;
  min-width: 200px;
}
.fund-item .fund-detail {
  font-size: 0.78rem;
  color: #57606a;
}
.fund-item .fund-amount {
  font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
  font-size: 0.82rem;
  font-weight: 700;
  color: #1f883d;
  white-space: nowrap;
}

/* ── Link grid ── */
.link-grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.6rem;
  margin: 1rem 0;
}
@media (max-width: 600px) {
  .link-grid { grid-template-columns: 1fr 1fr; }
}
.link-card {
  background: #f6f8fa;
  border: 1px solid #d0d7de;
  border-radius: 6px;
  padding: 0.7rem 0.9rem;
  text-align: center;
  text-decoration: none;
  color: #065f46;
  font-size: 0.82rem;
  font-weight: 600;
  transition: border-color 0.2s, background 0.2s;
  display: block;
}
.link-card:hover {
  border-color: #065f46;
  background: #eef1f4;
  text-decoration: none;
}
.link-card .lc-icon {
  font-size: 1.2rem;
  display: block;
  margin-bottom: 0.2rem;
}
.link-card .lc-sub {
  font-size: 0.7rem;
  color: #57606a;
  font-weight: 400;
}

/* ── Footer ── */
.cv-footer {
  background: linear-gradient(160deg, #064e3b 0%, #065f46 50%, #047857 100%);
  color: #a7f3d0;
  border-radius: 8px;
  padding: 1.2rem 1.5rem;
  margin-top: 2rem;
  text-align: center;
  font-size: 0.85rem;
  border: 1px solid #10b981;
}
.cv-footer a {
  color: #6ee7b7;
  text-decoration: none;
}
.cv-footer a:hover {
  text-decoration: underline;
}
.cv-footer .footer-quote {
  font-style: italic;
  color: #ecfdf5;
  margin-bottom: 0.5rem;
}
</style>

<!-- ═══════════ HERO ═══════════ -->
<div class="cv-hero">
  <div class="cv-name">Kun SUN 孙坤</div>
  <div class="cv-title">Full Tenured Professor of Computational Linguistics</div>
  <div class="cv-affil">Director, Institute of AI and Language Science · Tongji University, Shanghai</div>
  <div class="cv-contact">
    📧 kunsun@tongji.edu.cn · 📱 (+86) 18868115110 · 🌐 <a href="https://kevsuncl.github.io">kevsuncl.github.io</a>
  </div>
</div>

<!-- ═══════════ STATS ═══════════ -->
<div class="cv-stats">
  <div class="cv-pill">
    <div class="pill-num">40+</div>
    <div class="pill-lbl">Journal Papers</div>
  </div>
  <div class="cv-pill">
    <div class="pill-num">160K+</div>
    <div class="pill-lbl">HuggingFace Downloads</div>
  </div>
  <div class="cv-pill">
    <div class="pill-num">30+</div>
    <div class="pill-lbl">Open-Source Tools</div>
  </div>
  <div class="cv-pill">
    <div class="pill-num">15+</div>
    <div class="pill-lbl">Corpora (11+ Languages)</div>
  </div>
  <div class="cv-pill">
    <div class="pill-num">50+</div>
    <div class="pill-lbl">Students Supervised</div>
  </div>
</div>

<!-- ═══════════ ACADEMIC POSITIONS ═══════════ -->
<div class="cv-section">💼 Academic Positions</div>

<div class="cv-timeline">
  <div class="cv-tl-item active">
    <div class="tl-role">Director, Institute of AI and Language Science</div>
    <div class="tl-org">Tongji University, Shanghai</div>
    <span class="tl-date">11.2025 – present</span>
  </div>
  <div class="cv-tl-item active">
    <div class="tl-role">Full Tenured Professor of Computational Linguistics</div>
    <div class="tl-org">Tongji University, Shanghai</div>
    <span class="tl-date">09.2024 – present</span>
  </div>
  <div class="cv-tl-item">
    <div class="tl-role">Adjunct Professorial Research Fellow</div>
    <div class="tl-org">Fudan University, Shanghai</div>
    <span class="tl-date">03.2024 – present</span>
  </div>
  <div class="cv-tl-item">
    <div class="tl-role">Senior Scientist / Assistant Professor (Akademischer Rat)</div>
    <div class="tl-org">University of Tübingen, Germany</div>
    <span class="tl-date">10.2017 – 02.2025</span>
  </div>
  <div class="cv-tl-item">
    <div class="tl-role">Associate Professorial Research Fellow</div>
    <div class="tl-org">Zhejiang University, Hangzhou</div>
    <span class="tl-date">08.2016 – 08.2018</span>
  </div>
  <div class="cv-tl-item">
    <div class="tl-role">Associate Professor</div>
    <div class="tl-org">Zhejiang International Studies University, Hangzhou</div>
    <span class="tl-date">08.2013 – 08.2016</span>
  </div>
  <div class="cv-tl-item">
    <div class="tl-role">Lecturer</div>
    <div class="tl-org">Taizhou University, Taizhou</div>
    <span class="tl-date">08.2007 – 08.2013</span>
  </div>
</div>

<!-- ═══════════ EDUCATION ═══════════ -->
<div class="cv-section">🎓 Education</div>

<div class="cv-timeline">
  <div class="cv-tl-item">
    <div class="tl-role">Habilitation of Computational Linguistics (Professor Qualification)</div>
    <div class="tl-org">University of Tübingen, Germany</div>
    <span class="tl-date">10.2017 – 06.2024</span>
  </div>
  <div class="cv-tl-item">
    <div class="tl-role">Ph.D., (Computational) Linguistics</div>
    <div class="tl-org">East China Normal University, Shanghai</div>
    <span class="tl-date">09.2009 – 06.2012</span>
  </div>
  <div class="cv-tl-item">
    <div class="tl-role">M.A., Corpus Linguistics</div>
    <div class="tl-org">East China Normal University, Shanghai</div>
    <span class="tl-date">09.2004 – 07.2007</span>
  </div>
  <div class="cv-tl-item">
    <div class="tl-role">B.A., English Linguistics (minor: Statistics)</div>
    <div class="tl-org">Anhui Normal University, Wuhu</div>
    <span class="tl-date">09.2000 – 07.2004</span>
  </div>
</div>

**Other Academic Training:**
- 10th Fall School in Computational Linguistics, Stuttgart University (Sept 2019)
- European Summer School in Logic, Language and Information, University of Latvia (Aug 2019)
- Summer School of Tech & Media Communication, Open University & Cranfield University, U.K. (2014)
- Visiting PhD Student, Center for Chinese Languages, Peking University (02.2011 – 01.2012)
- Visiting Scholar, Dept. of Linguistics, University of Manchester, U.K. (09.2010 – 01.2011)

<!-- ═══════════ RESEARCH INTERESTS ═══════════ -->
<div class="cv-section">🔬 Research Interests</div>

<div class="ri-group">
  <div class="ri-title">Digital Humanities & Computational Text Analysis</div>
  <div class="ri-desc">Formal and computational models of discourse structure; computational measurement of coherence, cohesion, and information flow; graph-based and network representations of discourse; discourse dependency and cross-framework conversion (RST, PDTB, dependency); multilingual discourse parsing; distant reading and large-scale diachronic analysis of literary and scholarly texts; computational modeling of lexical semantic change and language evolution.</div>
</div>

<div class="ri-group">
  <div class="ri-title">Computational Linguistics & NLP</div>
  <div class="ri-desc">Fine-tuning and adaptation of LLMs for philological and humanistic research; neural-symbolic prompting & reasoning; hyper-dimensional & structured semantic representations; emotion and personality detection (text + multimodal); automatic essay scoring and feedback systems; machine translation evaluation for literary and scholarly texts.</div>
</div>

<div class="ri-group">
  <div class="ri-title">AI Methods, Ethics & Didactics</div>
  <div class="ri-desc">Efficient training & inference in LLMs; evaluations and benchmarking of AI models; cognitive-inspired reasoning in LLMs; critical assessment of AI biases, cultural tendencies, and societal impacts; development of DH-related curricula integrating AI literacy and ethical reflection.</div>
</div>

<div class="ri-group">
  <div class="ri-title">Computational Cognitive Science</div>
  <div class="ri-desc">Computational theories of cognition and learning; mechanistic and predictive models of human cognition; computational modeling of multilingual and multimodal language processing; neuro-computational models linking behavior, eye-tracking, EEG, MEG, and fMRI signals; discriminative and error-driven learning models.</div>
</div>

<div class="ri-group">
  <div class="ri-title">Computational Social Science</div>
  <div class="ri-desc">Sociolinguistic stratification and historical corpus analysis; sentiment analysis; AI-aided social network modeling; AI safety, ethics, and social impacts.</div>
</div>

<div class="ri-group">
  <div class="ri-title">Data Analysis & Statistical Methods</div>
  <div class="ri-desc">Large-scale data collection, curation, and mining; advanced statistical modeling (mixed-effects regression, GAM/GAMM, Bayesian hierarchical modeling); time-series and longitudinal models; causal inference; model comparison and robustness analysis.</div>
</div>

<!-- ═══════════ GRANTS & FUNDING ═══════════ -->
<div class="cv-section">💰 Grants & Funding</div>

**As Principal Investigator:**

<div class="fund-item">
  <div>
    <div class="fund-name">China National Science Grant</div>
    <div class="fund-detail">Attention-aware computational metrics for human multimodal language processing · No. 62512398 · 2025</div>
  </div>
  <div class="fund-amount">¥500K</div>
</div>

<div class="fund-item">
  <div>
    <div class="fund-name">National Social Science Fund of China</div>
    <div class="fund-detail">Investigating Chinese discourse structure through topic chain and event knowledge · No. 15YY038 · 2015–2020</div>
  </div>
  <div class="fund-amount">¥200K</div>
</div>

<div class="fund-item">
  <div>
    <div class="fund-name">China Postdoctoral Science Foundation, Outstanding Fund</div>
    <div class="fund-detail">Computational-cognitive studies on run-on sentences in Chinese · No. 2018T110581 · 2017–2020</div>
  </div>
  <div class="fund-amount">¥150K</div>
</div>

<div class="fund-item">
  <div>
    <div class="fund-name">Social Science Fund of Zhejiang Province</div>
    <div class="fund-detail">The textual function of topic chains and its application in translation · No. 13NDYB145 · 2013–2015</div>
  </div>
  <div class="fund-amount">¥30K</div>
</div>

<div class="fund-item">
  <div>
    <div class="fund-name">Zhejiang Provincial Social Science Association</div>
    <div class="fund-detail">A computational approach to commas in Chinese texts · No. 2012N067 · 2012–2014</div>
  </div>
  <div class="fund-amount">¥9K</div>
</div>

<div class="fund-item">
  <div>
    <div class="fund-name">Education Fund of Zhejiang Province</div>
    <div class="fund-detail">"One-stop" English teaching platform via multimedia network · No. 2014SCG090 · 2012–2015</div>
  </div>
  <div class="fund-amount">¥5K</div>
</div>

**As Co-PI / Member:**

<div class="fund-item">
  <div>
    <div class="fund-name">National Social Science Fund of China</div>
    <div class="fund-detail">The complex structure of news texts in Chinese · No. 18BYY184 · Co-PI</div>
  </div>
  <div class="fund-amount">¥200K</div>
</div>

<div class="fund-item">
  <div>
    <div class="fund-name">European Research Council (ERC) Advanced Project</div>
    <div class="fund-detail">Wide Incremental learning with Discrimination nEtworks · No. 742545 · Member</div>
  </div>
  <div class="fund-amount">€2.5M</div>
</div>

<!-- ═══════════ SELECTED PUBLICATIONS ═══════════ -->
<div class="cv-section">📚 Selected Recent Publications</div>

<p><em>* indicates corresponding author · Full list: <a href="https://scholar.google.com/citations?user=zE_8aHUAAAAJ&hl=en">Google Scholar</a></em></p>

**Peer-Reviewed Journal Papers (2022–2026):**

<div class="cv-card">
  <h4>[J1] Journal of Artificial Intelligence Research (2026)</h4>
  <p>Sun, K. & Wang, R. A novel dependency framework for enhancing discourse data analysis.</p>
</div>

<div class="cv-card">
  <h4>[J2] IEEE Trans. Cognitive Development and System (2026)</h4>
  <p>Sun, K. & Wang, R. The roles of contextual semantic relevance metrics in human visual processing.</p>
</div>

<div class="cv-card">
  <h4>[J3] Linguistics (2026)</h4>
  <p>Sun, K., Wang, R., & Baayen, H. Semantic coherence predicts reading fixation durations across languages beyond surprisal and lexical factors.</p>
</div>

<div class="cv-card">
  <h4>[J4] Language and Cognition (2026)</h4>
  <p>Sun, K. The ebb and flow of discourse connectives: Stylistic change or cognitive decline?</p>
</div>

<div class="cv-card">
  <h4>[J5] Neurocomputing (2025)</h4>
  <p>Sun, K. & Wang, R. Breaking myths in LLM scaling and emergent abilities with a comprehensive statistical analysis.</p>
</div>

<div class="cv-card">
  <h4>[J6] Neural Networks (2025)</h4>
  <p>Wang, R. & Sun, K.* A pipeline of neural-symbolic integration to enhance spatial reasoning in large language models.</p>
</div>

<div class="cv-card">
  <h4>[J7] Cognitive Science (2024)</h4>
  <p>Sun, K. & Wang, R. Computational sentence-level metrics for predicting human sentence comprehension.</p>
</div>

<div class="cv-card">
  <h4>[J8] Cognition (2024)</h4>
  <p>Sun, K. & Liu, H. Attention-aware semantic relevance predicting Chinese sentence reading.</p>
</div>

<div class="cv-card">
  <h4>[J13] PNAS (2022) <span class="cv-tag cv-tag-amber">Featured by MIT Technology Review</span></h4>
  <p>Sun, K. Colloquialization as a key factor in historical changes of rational and emotional words.</p>
</div>

<!-- ═══════════ TECHNICAL SKILLS ═══════════ -->
<div class="cv-section">🛠️ Technical Skills</div>

**Programming:**
<div class="cv-tags">
  <span class="cv-tag cv-tag-green">Python (advanced)</span>
  <span class="cv-tag cv-tag-green">R (advanced)</span>
  <span class="cv-tag cv-tag-green">PyTorch (advanced)</span>
  <span class="cv-tag cv-tag-green">LaTeX (advanced)</span>
  <span class="cv-tag cv-tag-green">Linux Shell (advanced)</span>
  <span class="cv-tag cv-tag-blue">JavaScript (intermediate)</span>
  <span class="cv-tag cv-tag-blue">HTML (intermediate)</span>
</div>

**Experimentation:**
<div class="cv-tags">
  <span class="cv-tag cv-tag-purple">Eye-tracker</span>
  <span class="cv-tag cv-tag-purple">EEG</span>
  <span class="cv-tag cv-tag-purple">Electromagnetic Articulography</span>
  <span class="cv-tag cv-tag-purple">Online experiments</span>
  <span class="cv-tag cv-tag-purple">E-Prime</span>
</div>

**Natural Languages:**
<div class="cv-tags">
  <span class="cv-tag">Chinese (native)</span>
  <span class="cv-tag">English (fluent)</span>
  <span class="cv-tag">Japanese (intermediate)</span>
  <span class="cv-tag">German (intermediate)</span>
  <span class="cv-tag">Latin (preliminary)</span>
</div>

<!-- ═══════════ SOFTWARE & TOOLS ═══════════ -->
<div class="cv-section">💻 Software, Databases & Corpora Developed</div>

<div class="cv-card">
  <h4>Software & Tools</h4>
  <ul>
    <li>Automatic converter of discourse dependency from discourse corpora</li>
    <li>Analyzer of discourse complexity (syntactic and discourse levels)</li>
    <li>Unified annotation tool for mining PDTB and RST corpora</li>
    <li>Toolkit for visualizing discourse networks</li>
    <li>Toolkit for computing attention-aware computational measures across multiple languages</li>
    <li>AI agent for ZH-EN & EN-ZH literary and scholarly translation</li>
    <li>Synthesis pipeline for automatic linguistic annotations applicable to philological research</li>
  </ul>
</div>

<div class="cv-card">
  <h4>Databases</h4>
  <ul>
    <li>Historical frequencies for discourse connectives across languages (1820–2010)</li>
    <li>Norms of historical psychosemantic dimensions in English</li>
    <li>Sentimental properties of onomatopoeia in 28 languages</li>
  </ul>
</div>

<div class="cv-card">
  <h4>Corpora & LLMs</h4>
  <ul>
    <li>Corpus of English hyphenated compounds</li>
    <li>Balanced corpus of discourse dependency in 11 languages</li>
    <li>Corpus of Chinese textual "run-on" sentences with multi-layer annotations</li>
    <li>Fine-tuned LLMs for detecting personalities <span class="cv-tag cv-tag-green">160K downloads</span></li>
    <li>Fine-tuned LLMs for detecting mental health</li>
    <li>LLMs for grading English composition for IELTS and L2 <span class="cv-tag cv-tag-green">120K downloads</span></li>
    <li>Generative LLMs for diagnosing English writings for IELTS</li>
    <li>Synthesis software of automatic linguistic analysis using LLMs</li>
  </ul>
</div>

<!-- ═══════════ TEACHING ═══════════ -->
<div class="cv-section">🎓 Teaching</div>

<div class="cv-card">
  <h4>Tongji University (2025/2026 Winter & Summer Semester)</h4>
  <div class="cv-tags" style="margin-top: 0.4rem;">
    <span class="cv-tag cv-tag-blue">Introduction to Computational Linguistics</span>
    <span class="cv-tag cv-tag-blue">Advanced Natural Language Processing</span>
    <span class="cv-tag cv-tag-blue">Methods in Language Sciences</span>
    <span class="cv-tag cv-tag-blue">Project-based Digital Humanities</span>
  </div>
</div>

<div class="cv-card">
  <h4>University of Tübingen (2019–2023)</h4>
  <p>Text Linguistics and Discourse Processes · Computational Models in Linguistic Research · Language Changes & Variations · Quantitative Methods in Experimental Linguistics · Transformer-Based Language Models</p>
</div>

<div class="cv-card">
  <h4>Zhejiang International Studies University (2013–2016)</h4>
  <p>Contrastive Analysis of Chinese and English · Computer-Aided Translation · Corpus Linguistics · Language and Society · English Reading & Writing</p>
</div>

<div class="cv-card">
  <h4>Taizhou University (2007–2009)</h4>
  <p>Introduction to Linguistics · English Reading & Writing · L2 Learning Strategies</p>
</div>

<!-- ═══════════ AWARDS ═══════════ -->
<div class="cv-section">🏅 Awards & Achievements</div>

<div class="award-item">
  <span class="aw-year">2016</span>
  <span class="aw-text"><strong>"Zhijiang Young Scholar of Social Sciences"</strong>, Zhejiang Province</span>
</div>
<div class="award-item">
  <span class="aw-year">2015–17</span>
  <span class="aw-text"><strong>"Advanced Research Worker" Award</strong>, Zhejiang International Studies University</span>
</div>
<div class="award-item">
  <span class="aw-year">2016</span>
  <span class="aw-text"><strong>Second Prize, "Teaching Achievement"</strong>, Zhejiang International Studies University</span>
</div>
<div class="award-item">
  <span class="aw-year">2014</span>
  <span class="aw-text"><strong>"Outstanding Teacher"</strong>, Zhejiang International Studies University</span>
</div>
<div class="award-item">
  <span class="aw-year">2010–12</span>
  <span class="aw-text"><strong>"National First Class Scholarship"</strong>, East China Normal University</span>
</div>

<!-- ═══════════ EDITORIAL & SERVICE ═══════════ -->
<div class="cv-section">📝 Journal Editorial Roles & Academic Service</div>

**Editorial Boards:**
<div class="cv-tags" style="margin-bottom: 0.8rem;">
  <span class="cv-tag cv-tag-purple">Review Editor · Frontiers in Psychology</span>
  <span class="cv-tag cv-tag-purple">Editorial Board · Scientific Reports</span>
  <span class="cv-tag cv-tag-purple">Editorial Board · BMC Psychology</span>
</div>

**Reviewing:** Reviewer for **80+ international SSCI/SCI journals** including *Psychological Science*, *Nature Human Behavior*, *Cognitive Science*, *Linguistics*, *Big Data & Society*, *PLoS ONE*, *IEEE Access*. Reviewer for top AI conferences: *ACL*, *EMNLP*, *ICML*. Reviewer for National Social Science Funding of China and National Science Funding of Poland.

**Service:**
- Supervised approx. 50 bachelor and master theses since 2010
- Co-supervised two PhD dissertations (Huiyuan Jin, Yalan Wang), 07.2017–12.2021
- Organized the International Morphological Processing Conference, Tübingen (Nov 2019)
- Organizer, Academic Forum, Zhejiang International Studies University (2013–2016)
- Temporary Coordinator, Collaborative Innovation Center, Zhejiang University (2016–2017)

<!-- ═══════════ LINKS ═══════════ -->
<div class="cv-section">🔗 Professional Networks</div>

<div class="link-grid">
  <a class="link-card" href="https://scholar.google.com/citations?user=zE_8aHUAAAAJ&hl=en">
    <span class="lc-icon">📊</span>Google Scholar
    <span class="lc-sub">Publications & Citations</span>
  </a>
  <a class="link-card" href="https://orcid.org/0000-0001-9766-269X">
    <span class="lc-icon">🆔</span>ORCID
    <span class="lc-sub">0000-0001-9766-269X</span>
  </a>
  <a class="link-card" href="https://www.researchgate.net/profile/Kun_Sun15">
    <span class="lc-icon">🔬</span>ResearchGate
    <span class="lc-sub">Research Profile</span>
  </a>
  <a class="link-card" href="https://github.com/fivehills">
    <span class="lc-icon">💻</span>GitHub
    <span class="lc-sub">@fivehills</span>
  </a>
  <a class="link-card" href="https://huggingface.co/KevSun">
    <span class="lc-icon">🤗</span>Hugging Face
    <span class="lc-sub">@KevSun</span>
  </a>
  <a class="link-card" href="https://linkedin.com/in/kun-sun-mlds">
    <span class="lc-icon">🔗</span>LinkedIn
    <span class="lc-sub">kun-sun-mlds</span>
  </a>
</div>

<!-- ═══════════ FOOTER ═══════════ -->
<div class="cv-footer">
  <div class="footer-quote">"Bridging the gap between human cognition and artificial intelligence through computational linguistics and cognitive science."</div>
  📧 kunsun@tongji.edu.cn · 🌐 <a href="https://kevsuncl.github.io">kevsuncl.github.io</a>
</div>

---

*Last updated: March 2026*
