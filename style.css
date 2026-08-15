/* ============================================
   TOKENS
   ============================================ */
:root {
  --bg: #0a0e17;
  --surface: #121826;
  --surface-2: #1a2233;
  --border: #232c40;
  --text: #edeff3;
  --text-muted: #8a93a8;
  --text-faint: #545e75;

  --accent: #e8a33d;        /* signal amber — code mode */
  --accent-soft: #e8a33d22;
  --accent-rgb: 232, 163, 61;

  --font-display: "Newsreader", serif;
  --font-body: "Work Sans", sans-serif;
  --font-mono: "JetBrains Mono", monospace;
  --font-urdu: "Noto Nastaliq Urdu", serif;

  --radius: 3px;
  --transition-mode: 0.6s cubic-bezier(0.65, 0, 0.35, 1);
}

/* shayari mode palette */
body.shayari-mode {
  --accent: #d46a82;        /* ghazal rose */
  --accent-soft: #d46a8222;
  --accent-rgb: 212, 106, 130;
}

* { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--font-body);
  font-size: 16px;
  line-height: 1.6;
  overflow-x: hidden;
  transition: background 0.6s ease;
}

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  * { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; }
}

a { color: inherit; text-decoration: none; }
ul { list-style: none; }

::selection { background: var(--accent); color: #0a0e17; }

/* custom cursor dot (desktop only) */
.cursor-dot {
  position: fixed;
  width: 8px; height: 8px;
  border-radius: 50%;
  background: var(--accent);
  pointer-events: none;
  z-index: 9999;
  transform: translate(-50%, -50%);
  transition: background 0.4s ease, width 0.2s ease, height 0.2s ease;
  mix-blend-mode: difference;
  display: none;
}
@media (hover: hover) and (pointer: fine) {
  .cursor-dot { display: block; }
}

.noise {
  position: fixed; inset: 0;
  pointer-events: none;
  z-index: 1;
  opacity: 0.035;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
}

/* ============================================
   NAVIGATION
   ============================================ */
#navbar {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  background: rgba(10, 14, 23, 0.75);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--border);
}

.nav-inner {
  max-width: 1200px;
  margin: 0 auto;
  padding: 18px 32px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
}

.nav-logo {
  font-family: var(--font-mono);
  font-weight: 700;
  font-size: 1.1rem;
  letter-spacing: 0.5px;
}
.nav-logo .dot { color: var(--accent); }

.nav-links {
  display: flex;
  gap: 28px;
  font-family: var(--font-mono);
  font-size: 0.82rem;
  color: var(--text-muted);
}
.nav-links a { position: relative; transition: color 0.3s ease; }
.nav-links a::before { content: "// "; color: var(--accent); opacity: 0; transition: opacity 0.2s ease; }
.nav-links a:hover { color: var(--text); }
.nav-links a:hover::before { opacity: 1; }

.mode-toggle {
  display: flex;
  align-items: center;
  gap: 10px;
  cursor: pointer;
  user-select: none;
}
.mode-track {
  width: 44px; height: 22px;
  background: var(--surface-2);
  border: 1px solid var(--border);
  border-radius: 20px;
  position: relative;
  transition: border-color 0.4s ease;
}
.mode-thumb {
  position: absolute;
  top: 2px; left: 2px;
  width: 16px; height: 16px;
  border-radius: 50%;
  background: var(--accent);
  transition: transform var(--transition-mode), background 0.4s ease;
}
body.shayari-mode .mode-thumb { transform: translateX(22px); }

.mode-label {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  color: var(--text-muted);
  min-width: 78px;
}

.nav-burger {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 6px;
}
.nav-burger span { width: 20px; height: 2px; background: var(--text); }

.mobile-menu {
  display: none;
  position: fixed;
  top: 61px; left: 0; right: 0;
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  z-index: 99;
  flex-direction: column;
  padding: 16px 32px 24px;
}
.mobile-menu.open { display: flex; }
.mobile-menu a {
  padding: 12px 0;
  font-family: var(--font-mono);
  font-size: 0.9rem;
  color: var(--text-muted);
  border-bottom: 1px solid var(--border);
}

/* ============================================
   LAYOUT HELPERS
   ============================================ */
.section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 120px 32px;
  position: relative;
  z-index: 2;
}
.section.alt { background: var(--surface); }
.section.alt { max-width: 100%; }
.section.alt > * { max-width: 1200px; margin-left: auto; margin-right: auto; }
.section.alt { padding-left: 0; padding-right: 0; }
.section.alt .section-eyebrow,
.section.alt .section-title,
.section.alt .skills-grid,
.section.alt .timeline { padding-left: 32px; padding-right: 32px; }

.section-eyebrow {
  font-family: var(--font-mono);
  font-size: 0.78rem;
  color: var(--accent);
  letter-spacing: 1px;
  margin-bottom: 16px;
  transition: color 0.4s ease;
}

.section-title {
  font-family: var(--font-display);
  font-weight: 500;
  font-size: clamp(2rem, 4vw, 3rem);
  line-height: 1.15;
  margin-bottom: 48px;
  max-width: 700px;
}

.accent-word {
  font-style: italic;
  color: var(--accent);
  transition: color 0.4s ease;
}

.urdu { font-family: var(--font-urdu); font-size: 1.1em; }

/* ============================================
   HERO
   ============================================ */
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 140px 32px 80px;
  position: relative;
  z-index: 2;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 60px;
  align-items: center;
}

.eyebrow {
  font-family: var(--font-mono);
  color: var(--accent);
  font-size: 0.9rem;
  margin-bottom: 20px;
  transition: color 0.4s ease;
}
.blink-cursor {
  display: inline-block;
  animation: blink 1s step-end infinite;
}
@keyframes blink { 50% { opacity: 0; } }

.hero-name {
  font-family: var(--font-display);
  font-weight: 500;
  font-size: clamp(3rem, 8vw, 5.5rem);
  line-height: 0.98;
  margin-bottom: 24px;
}
.hero-name .line { display: block; }
.hero-name .accent-word {
  font-style: italic;
}

.hero-role {
  font-family: var(--font-mono);
  font-size: 1rem;
  color: var(--text);
  margin-bottom: 18px;
}

.hero-desc {
  color: var(--text-muted);
  font-size: 1.05rem;
  max-width: 480px;
  margin-bottom: 36px;
}
.hero-desc strong { color: var(--text); font-weight: 600; }

.hero-cta { display: flex; gap: 16px; flex-wrap: wrap; }

.btn {
  font-family: var(--font-mono);
  font-size: 0.85rem;
  padding: 14px 26px;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  transition: all 0.3s ease;
  display: inline-block;
}
.btn-primary {
  background: var(--accent);
  color: #0a0e17;
  border-color: var(--accent);
  font-weight: 600;
}
.btn-primary:hover { filter: brightness(1.1); transform: translateY(-2px); }
.btn-ghost {
  color: var(--text);
  background: transparent;
}
.btn-ghost:hover { border-color: var(--accent); color: var(--accent); }

/* terminal */
.terminal {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 30px 60px -20px rgba(0,0,0,0.6);
}
.terminal-bar {
  background: var(--surface-2);
  padding: 10px 14px;
  display: flex;
  align-items: center;
  gap: 8px;
  border-bottom: 1px solid var(--border);
}
.tdot { width: 10px; height: 10px; border-radius: 50%; }
.tdot.r { background: #e05a5a; }
.tdot.y { background: #e8b23d; }
.tdot.g { background: #5ac47e; }
.terminal-title {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--text-faint);
  margin-left: 8px;
}
.terminal-body {
  padding: 22px;
  font-family: var(--font-mono);
  font-size: 0.85rem;
  color: var(--text-muted);
}
.terminal-body .prompt { color: var(--accent); }
.terminal-body pre {
  color: var(--text);
  margin: 12px 0;
  white-space: pre-wrap;
  font-family: var(--font-mono);
}
.typing-cursor { animation: blink 1s step-end infinite; color: var(--accent); }

.scroll-hint {
  position: absolute;
  bottom: 32px; left: 32px;
  display: flex;
  align-items: center;
  gap: 10px;
  font-family: var(--font-mono);
  font-size: 0.7rem;
  color: var(--text-faint);
  letter-spacing: 1px;
}
.scroll-line { width: 32px; height: 1px; background: var(--text-faint); }

/* ============================================
   ABOUT
   ============================================ */
.about-grid {
  display: grid;
  grid-template-columns: 1.3fr 1fr;
  gap: 60px;
}
.about-text p { color: var(--text-muted); margin-bottom: 20px; max-width: 560px; }
.about-tags { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 24px; }
.tag {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--text-muted);
  border: 1px solid var(--border);
  padding: 6px 12px;
  border-radius: 20px;
}

.about-stats {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  align-content: start;
}
.stat-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 24px 20px;
}
.stat-num {
  display: block;
  font-family: var(--font-display);
  font-size: 2.2rem;
  color: var(--accent);
  transition: color 0.4s ease;
}
.stat-label {
  display: block;
  font-size: 0.82rem;
  color: var(--text-muted);
  margin-top: 6px;
}

/* ============================================
   SKILLS
   ============================================ */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 40px;
}
.skill-group h3 {
  font-family: var(--font-mono);
  font-size: 0.85rem;
  color: var(--text);
  margin-bottom: 16px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--border);
}
.chip-row { display: flex; flex-wrap: wrap; gap: 10px; }
.chip {
  font-size: 0.82rem;
  padding: 8px 14px;
  border-radius: var(--radius);
  background: var(--surface-2);
  border: 1px solid var(--border);
  color: var(--text-muted);
  transition: border-color 0.3s ease, color 0.3s ease;
}
.chip:hover { border-color: var(--accent); color: var(--text); }
.chip.small { font-size: 0.72rem; padding: 6px 10px; }

/* ============================================
   PROJECTS
   ============================================ */
.project-list { display: flex; flex-direction: column; gap: 20px; }
.project-card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 36px;
  transition: border-color 0.3s ease, transform 0.3s ease;
}
.project-card:hover { border-color: var(--accent); transform: translateX(4px); }
.project-card.featured { border-color: var(--accent-soft); background: linear-gradient(135deg, var(--surface), var(--surface-2)); }
.project-kicker {
  font-family: var(--font-mono);
  font-size: 0.72rem;
  color: var(--accent);
  letter-spacing: 1px;
  margin-bottom: 10px;
  transition: color 0.4s ease;
}
.project-card h3 { font-family: var(--font-display); font-size: 1.6rem; font-weight: 500; margin-bottom: 12px; }
.project-desc { color: var(--text-muted); max-width: 680px; margin-bottom: 16px; }
.project-points { margin: 0 0 20px 0; }
.project-points li {
  color: var(--text-muted);
  font-size: 0.9rem;
  padding-left: 18px;
  position: relative;
  margin-bottom: 8px;
  max-width: 680px;
}
.project-points li::before {
  content: "→";
  position: absolute;
  left: 0;
  color: var(--accent);
}

/* ============================================
   TIMELINE
   ============================================ */
.timeline { position: relative; max-width: 800px; }
.timeline::before {
  content: "";
  position: absolute;
  left: 6px; top: 6px; bottom: 6px;
  width: 1px;
  background: var(--border);
}
.tl-item { position: relative; padding-left: 40px; margin-bottom: 44px; }
.tl-item:last-child { margin-bottom: 0; }
.tl-dot {
  position: absolute;
  left: 0; top: 4px;
  width: 13px; height: 13px;
  border-radius: 50%;
  background: var(--bg);
  border: 2px solid var(--accent);
  transition: border-color 0.4s ease;
}
.tl-date {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--accent);
  margin-bottom: 6px;
  transition: color 0.4s ease;
}
.tl-content h3 { font-size: 1.15rem; font-weight: 600; margin-bottom: 4px; }
.tl-org { color: var(--text-muted); font-size: 0.88rem; margin-bottom: 10px; font-family: var(--font-mono); }
.tl-desc { color: var(--text-muted); max-width: 560px; font-size: 0.92rem; }

/* ============================================
   CERTIFICATIONS
   ============================================ */
.cert-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}
.cert-card {
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 28px;
  transition: border-color 0.3s ease;
}
.cert-card:hover { border-color: var(--accent); }
.cert-icon { color: var(--accent); font-size: 1.2rem; transition: color 0.4s ease; }
.cert-card h3 { font-size: 1.05rem; margin: 12px 0 8px; font-weight: 600; }
.cert-card p { color: var(--text-muted); font-size: 0.88rem; }

/* ============================================
   SHAYARI SECTION — hidden in code mode
   ============================================ */
.shayari-section {
  text-align: center;
  padding-top: 60px;
  padding-bottom: 60px;
  max-height: 0;
  opacity: 0;
  overflow: hidden;
  padding-top: 0;
  padding-bottom: 0;
  transition: max-height 0.7s ease, opacity 0.5s ease, padding 0.7s ease;
}
body.shayari-mode .shayari-section {
  max-height: 500px;
  opacity: 1;
  padding-top: 100px;
  padding-bottom: 40px;
}
.shayari-section .section-eyebrow { text-align: center; }
.urdu-title {
  font-family: var(--font-urdu);
  font-size: 2.4rem;
  margin: 0 auto 32px;
  color: var(--accent);
}
.couplet {
  font-family: var(--font-urdu);
  font-size: 1.6rem;
  line-height: 2.1;
  color: var(--text);
  max-width: 600px;
  margin: 0 auto;
}
.couplet-note {
  margin-top: 20px;
  color: var(--text-muted);
  font-family: var(--font-mono);
  font-size: 0.85rem;
}

/* ============================================
   CONTACT
   ============================================ */
.contact-section { text-align: left; }
.contact-sub { color: var(--text-muted); margin-bottom: 48px; max-width: 500px; }
.contact-form { max-width: 560px; }
.form-row { margin-bottom: 20px; display: flex; flex-direction: column; gap: 8px; }
.form-row label {
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--text-muted);
}
.form-row input, .form-row textarea {
  background: var(--surface-2);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 14px 16px;
  color: var(--text);
  font-family: var(--font-body);
  font-size: 0.95rem;
  resize: vertical;
  transition: border-color 0.3s ease;
}
.form-row input:focus, .form-row textarea:focus {
  outline: none;
  border-color: var(--accent);
}
.form-status {
  margin-top: 14px;
  font-family: var(--font-mono);
  font-size: 0.82rem;
  color: var(--accent);
  min-height: 1em;
  transition: color 0.4s ease;
}

.social-row {
  display: flex;
  gap: 24px;
  margin-top: 48px;
  font-family: var(--font-mono);
  font-size: 0.85rem;
}
.social-row a { color: var(--text-muted); border-bottom: 1px solid transparent; transition: all 0.3s ease; }
.social-row a:hover { color: var(--accent); border-color: var(--accent); }

/* ============================================
   FOOTER
   ============================================ */
footer {
  text-align: center;
  padding: 40px 32px;
  border-top: 1px solid var(--border);
  color: var(--text-faint);
  font-family: var(--font-mono);
  font-size: 0.78rem;
}

/* ============================================
   SCROLL REVEAL
   ============================================ */
.reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.7s ease, transform 0.7s ease; }
.reveal.visible { opacity: 1; transform: translateY(0); }

/* ============================================
   RESPONSIVE
   ============================================ */
@media (max-width: 900px) {
  .hero-grid { grid-template-columns: 1fr; }
  .about-grid { grid-template-columns: 1fr; }
  .skills-grid { grid-template-columns: 1fr; }
  .cert-grid { grid-template-columns: 1fr; }
  .nav-links { display: none; }
  .nav-burger { display: flex; }
  .about-stats { grid-template-columns: 1fr 1fr; }
}

@media (max-width: 560px) {
  .section { padding: 90px 22px; }
  .hero { padding: 120px 22px 60px; }
  .nav-inner { padding: 16px 20px; }
  .mode-label { display: none; }
  .about-stats { grid-template-columns: 1fr; }
  .project-card { padding: 26px; }
}
