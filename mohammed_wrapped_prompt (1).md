# 🎧 Portfolio Wrapped — Prompt File for Claude Haiku 4.5

> Feed this entire file as the user prompt to `claude-haiku-4-5-20251001` via the Anthropic API.  
> Model: `claude-haiku-4-5-20251001` | Max tokens: `4096` | Output: Single self-contained HTML file.

---

## SYSTEM PROMPT

```
You are an expert frontend developer and creative designer. You write production-grade, 
self-contained HTML files with embedded CSS and JavaScript. You have a strong aesthetic 
sensibility and build visually stunning, animated interfaces. You never use external 
frameworks beyond Google Fonts and you never produce placeholder content — everything 
is real, specific, and data-driven from what you are given.
```

---

## USER PROMPT

Build a **"Portfolio Wrapped"** — a Spotify Wrapped-style interactive story experience — 
for the following person. It should feel like a premium, cinematic year-in-review 
presentation: full-screen slides that auto-advance or respond to clicks, bold typography, 
rich animations, and data-driven storytelling pulled directly from the portfolio below.

---

### 👤 PORTFOLIO DATA

**Name:** Mohammed Omer Yousuf Ali  
**Award:** Outstanding Leadership Award — BITS Pilani, Dubai Campus  
**Contact:** +971 55 279 9632 · f20220155@dubai.bits-pilani.ac.in  
**Institution:** BITS Pilani, Dubai Campus, UAE

**Profile:**  
Experienced across design, marketing, entrepreneurship, and technology, with a consistent 
track record of taking initiative beyond his defined role. Thrives in environments that 
reward ownership. Builds communities where learning happens through action. Leads by doing.

**Leadership Roles (Chronological Order):**
- Creative Lead – GDSC, BITS Dubai (Feb–May 2024): Supported hackathons and workshops
- Creative Lead – Paribhasha Drama Club (Sep 2024–Present): Visual identity & production logistics
- Marketing Head – Alumni Relations Division (Sep 2024–Present): Led all alumni marketing campaigns
- Media Head – BITS Tech Fest 2024: Real-time live coverage across multi-day event
- Marketing Co-Head – Spectrum (2024–2025): Campaign strategy & sponsorship comms
- Co-Lead – Google Developer Groups (GDG), BITS Dubai (Oct 2024–Present): End-to-end event management, grew chapter
- Digital & Creative Head – BSF Core Committee (2025): Handled all creative for UAE's largest inter-college sports event
- Mentor – BITS Tech Fest 2025: Guiding the next organizing committee
- VP – Entrepreneurship Cell (2025–2026): Built entrepreneurial culture via events & speakers
- VP – Alumni Relations Division (2025–2026): Oversaw alumni engagement, ran JASHN reunion

**Professional Experience:**
- Creative & Omnichannel Excellence Intern – MSD GLE (Jan 2026–Present):  
  UI/website work → identified workflow inefficiencies → automated creative production → 
  extended automation to Salesforce Marketing Cloud → self-initiated OCR image indexing project using Tesseract
- Web Development & Sales Intern – Emqube LLC, Dubai (May–Jul 2024):  
  Built landing pages, ran a full marketing campaign end-to-end, managed client websites

---

### 🎨 DESIGN DIRECTION

**Aesthetic:** Dark, cinematic, maximalist — inspired by Spotify Wrapped but pushed further.  
Use a deep near-black background (`#0a0a0f`) with electric accent colors that shift per slide 
(acid green → hot coral → electric violet → golden amber → ice blue).  
Typography: Use Google Fonts — `Syne` (display/headings) + `DM Sans` (body).  
Every slide should have a distinct color accent but share the same dark base.

**Animation style:**
- Slide transitions: fast horizontal slide or scale-pop, 400ms cubic-bezier easing
- Numbers/stats: count-up animation when slide enters
- Text: staggered fade-up reveals, 80ms between each word or line
- Background: slow animated gradient mesh or particle drift (CSS only, no canvas libs)
- Progress bar at the bottom showing slide position

---

### 📊 SLIDES TO GENERATE

Generate exactly **10 slides** in this sequence. Each slide is full-screen (100vw × 100vh).

**Slide 1 — INTRO / TITLE**  
Bold opener. Name large. Award banner. Tagline: *"This is what a year of ownership looks like."*  
Accent: acid green `#00ff87`

**Slide 2 — BY THE NUMBERS**  
Show these stats with animated count-up:  
- `11` Leadership Roles  
- `2` VP Positions  
- `3+` Years of campus involvement  
- `2` Internships  
Big bold numbers, minimal labels. Headline: *"The numbers don't lie."*  
Accent: hot coral `#ff4d6d`

**Slide 3 — YOUR TOP SKILL: REAL-TIME DECISION MAKING**  
Pull quotes/evidence from the portfolio about on-ground, live-event decision making.  
Show 3 quick bullet fragments (not full sentences) flying in one-by-one.  
Headline: *"When plans change, you don't."*  
Accent: electric violet `#9b5de5`

**Slide 4 — DOMAINS YOU OWNED**  
Animated tag cloud or grid of domains:  
Design · Marketing · Entrepreneurship · Technology · Events · Media · Community · Automation  
Each tag pops in with a slight rotation bounce. Headline: *"You didn't pick a lane."*  
Accent: golden amber `#ffd60a`

**Slide 5 — BIGGEST MOMENT: JASHN & BSF**  
Split screen or layered card: one side for JASHN (Alumni Reunion), one for BSF (Sports Festival).  
Short punchy copy for each. Headline: *"Two of the UAE's biggest campus events. Both yours."*  
Accent: ice blue `#00b4d8`

**Slide 6 — INTERNSHIP SPOTLIGHT: MSD GLE**  
Timeline-style or flowing steps showing the progression at MSD:  
UI Work → Identified Inefficiency → Automated Workflows → SFMC Extension → OCR Project (self-initiated)  
Headline: *"You didn't wait to be asked."*  
Accent: acid green `#00ff87`

**Slide 7 — YOUR CREATIVE FOOTPRINT**  
Mosaic/grid of all the clubs and events where Mohammed led creative output:  
GDG · BSF · Drama Club · Tech Fest · Spectrum · Alumni Division  
Headline: *"Every campus touchpoint, shaped by you."*  
Accent: hot coral `#ff4d6d`

**Slide 8 — LEADERSHIP STYLE BREAKDOWN**  
Horizontal bar chart (CSS-only, animated width on enter) showing made-up-but-plausible  
"style percentages":  
- On-ground execution: 94%  
- Cross-team coordination: 88%  
- Creative direction: 91%  
- Initiative beyond role: 97%  
- Community building: 85%  
Headline: *"Your leadership profile."*  
Accent: electric violet `#9b5de5`

**Slide 9 — WHAT PEOPLE WOULD SAY**  
3 fake-but-plausible testimonial cards, short (1–2 lines each), from archetypes like:  
"A fellow VP", "An event attendee", "A team member".  
Cards slide in with stagger. Headline: *"The room noticed."*  
Accent: golden amber `#ffd60a`

**Slide 10 — CLOSING / OUTRO**  
Full-screen with name large again. Closing line:  
*"The award is proof. The work was the point."*  
Social / contact info subtle at bottom. Replay button to go back to slide 1.  
Accent: all accents cycling in a slow gradient animation.

---

### ⚙️ TECHNICAL REQUIREMENTS

- **Single HTML file** — all CSS and JS embedded, no external dependencies except Google Fonts CDN
- Slides stored as an array of objects in JS; rendered dynamically
- Navigation: click anywhere to advance, left arrow key to go back, right arrow to advance
- Mobile-responsive: works at 375px width (font sizes scale down)
- Slide counter visible (e.g. "3 / 10") in top-right corner
- Bottom progress bar (thin line) that fills as slides advance
- Smooth entrance animations per slide using `IntersectionObserver` or class toggling on active slide
- No jQuery, no React, no Vue — vanilla JS only
- All animations must use CSS transitions/keyframes (no GSAP, no anime.js)
- The HTML file must be fully functional when opened locally (no server required)

---

### 📦 OUTPUT FORMAT

Return **only** the complete HTML file content, starting with `<!DOCTYPE html>`.  
Do not include any explanation, preamble, markdown fences, or commentary.  
The file should be ready to save as `mohammed_wrapped.html` and open in a browser.
