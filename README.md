* {
  box-sizing: border-box;
}

:root {
  --bg: #07111f;
  --bg-alt: #0e1b2e;
  --panel: rgba(17, 29, 46, 0.9);
  --panel-strong: #101d2f;
  --card: rgba(11, 19, 29, 0.8);
  --primary: #7dd3fc;
  --primary-strong: #38bdf8;
  --text: #e5eefc;
  --muted: #a9bbd3;
  --line: rgba(164, 195, 232, 0.18);
  --shadow: 0 20px 60px rgba(8, 15, 29, 0.42);
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: "Inter", sans-serif;
  background:
    radial-gradient(circle at top, rgba(56, 189, 248, 0.18), transparent 30%),
    linear-gradient(180deg, #07111f 0%, #0a1423 100%);
  color: var(--text);
  line-height: 1.6;
}

a {
  color: inherit;
  text-decoration: none;
}

img {
  max-width: 100%;
  display: block;
}

.container {
  width: min(1100px, calc(100% - 2rem));
  margin: 0 auto;
}

.site-header {
  position: sticky;
  top: 0;
  z-index: 20;
  backdrop-filter: blur(12px);
  background: rgba(7, 17, 31, 0.65);
  border-bottom: 1px solid var(--line);
}

.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  min-height: 78px;
  gap: 1rem;
}

.brand {
  display: inline-flex;
  align-items: center;
  gap: 0.7rem;
  font-weight: 700;
  letter-spacing: -0.04em;
}

.brand-mark {
  width: 2rem;
  height: 2rem;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 0.7rem;
  background: linear-gradient(135deg, var(--primary), #5eead4);
  color: #06121d;
  font-weight: 800;
}

.main-nav {
  display: flex;
  align-items: center;
  gap: 1.2rem;
  color: var(--muted);
}

.main-nav a {
  transition: color 0.2s ease;
}

.main-nav a:hover {
  color: var(--text);
}

.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 999px;
  padding: 0.9rem 1.4rem;
  font-weight: 600;
  transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
}

.button:hover {
  transform: translateY(-1px);
}

.button-primary {
  background: linear-gradient(135deg, var(--primary), var(--primary-strong));
  color: #06121d;
  box-shadow: 0 12px 30px rgba(56, 189, 248, 0.35);
}

.button-secondary {
  border: 1px solid var(--line);
  background: rgba(255, 255, 255, 0.02);
  color: var(--text);
}

.hero {
  padding: 5rem 0 3rem;
}

.hero-grid {
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 2rem;
  align-items: center;
}

.eyebrow {
  margin: 0 0 0.8rem;
  color: var(--primary);
  text-transform: uppercase;
  letter-spacing: 0.12em;
  font-size: 0.8rem;
  font-weight: 700;
}

.hero-copy h1,
.section-heading h2,
.about-grid h2,
.site-footer h2 {
  margin: 0;
  letter-spacing: -0.06em;
  line-height: 1.0;
}

.hero-copy h1 {
  font-size: clamp(2.8rem, 6vw, 5rem);
  margin-bottom: 1rem;
}

.lead {
  max-width: 60ch;
  color: var(--muted);
  font-size: 1.08rem;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  margin: 2rem 0;
}

.hero-stats {
  list-style: none;
  padding: 0;
  margin: 2rem 0 0;
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

.hero-stats li {
  min-width: 120px;
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid var(--line);
  border-radius: 18px;
  padding: 0.9rem 1rem;
}

.hero-stats strong {
  display: block;
  font-size: 1.1rem;
  margin-bottom: 0.2rem;
}

.hero-stats span {
  color: var(--muted);
  font-size: 0.9rem;
}

.hero-panel {
  display: flex;
  justify-content: center;
}

.panel-window {
  width: min(100%, 520px);
  background: rgba(10, 18, 28, 0.9);
  border: 1px solid var(--line);
  border-radius: 24px;
  box-shadow: var(--shadow);
  overflow: hidden;
}

.window-bar {
  display: flex;
  gap: 0.5rem;
  align-items: center;
  height: 46px;
  padding: 0 1rem;
  background: rgba(255, 255, 255, 0.02);
  border-bottom: 1px solid var(--line);
}

.window-bar span {
  width: 0.75rem;
  height: 0.75rem;
  border-radius: 50%;
  display: inline-block;
}

.window-bar span:nth-child(1) { background: #f87171; }
.window-bar span:nth-child(2) { background: #fbbf24; }
.window-bar span:nth-child(3) { background: #4ade80; }

.window-body {
  padding: 1.25rem;
}

.code-block {
  background: rgba(5, 10, 16, 0.85);
  border: 1px solid var(--line);
  border-radius: 16px;
  padding: 1rem;
  overflow: auto;
}

.code-block pre {
  margin: 0;
  color: #d9f3ff;
  font-size: 0.86rem;
  line-height: 1.7;
}

.section {
  padding: 5rem 0;
}

.alt-section {
  background: rgba(255, 255, 255, 0.01);
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
}

.section-heading {
  margin-bottom: 2rem;
}

.section-heading h2,
.about-grid h2,
.site-footer h2 {
  font-size: clamp(2rem, 4vw, 3rem);
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 1.25rem;
}

.card {
  background: rgba(12, 20, 30, 0.8);
  border: 1px solid var(--line);
  border-radius: 22px;
  padding: 1.5rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.12);
}

.card-icon {
  display: inline-flex;
  min-width: 2.5rem;
  height: 2.5rem;
  border-radius: 12px;
  align-items: center;
  justify-content: center;
  background: rgba(125, 211, 252, 0.12);
  border: 1px solid rgba(125, 211, 252, 0.3);
  color: var(--primary);
  font-weight: 700;
  margin-bottom: 1rem;
}

.card h3 {
  margin: 0 0 0.7rem;
  font-size: 1.4rem;
}

.card p {
  margin: 0;
  color: var(--muted);
}

.steps {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 1rem;
}

.step {
  background: rgba(12, 20, 30, 0.8);
  border: 1px solid var(--line);
  border-radius: 20px;
  padding: 1.4rem;
}

.step span {
  display: inline-flex;
  width: 2.2rem;
  height: 2.2rem;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
  background: rgba(56, 189, 248, 0.12);
  border: 1px solid rgba(125, 211, 252, 0.45);
  color: var(--primary);
  font-weight: 700;
}

.step h3 {
  margin: 1rem 0 0.5rem;
}

.step p {
  margin: 0;
  color: var(--muted);
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
  gap: 2rem;
  align-items: start;
}

.about-grid p {
  color: var(--muted);
  margin: 0;
  font-size: 1.05rem;
}

.site-footer {
  padding: 4rem 0 1.5rem;
  border-top: 1px solid var(--line);
}

.footer-grid {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
  padding-bottom: 2rem;
}

.footer-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

.footer-bottom {
  border-top: 1px solid var(--line);
  padding-top: 1.2rem;
  color: var(--muted);
}

@media (max-width: 900px) {
  .hero-grid,
  .about-grid,
  .card-grid,
  .steps,
  .footer-grid {
    grid-template-columns: 1fr;
    display: grid;
  }

  .main-nav {
    display: none;
  }

  .footer-grid {
    display: grid;
  }
}

@media (max-width: 560px) {
  .hero {
    padding-top: 4rem;
  }

  .button {
    width: 100%;
  }

  .hero-actions,
  .footer-actions {
    display: grid;
    width: 100%;
  }
}






























































































































































 

a{"path":"script.js"} 