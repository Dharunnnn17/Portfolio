# Ex01 Portfolio
## Date: 30.10.2026

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
# Index.html
```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta
      name="description"
      content="The portfolio of Dharun Arulselvan, an Information Technology student who enjoys building and testing ideas."
    />
    <meta name="theme-color" content="#f5f4ef" />
    <title>Dharun Arulselvan — IT Student &amp; Builder</title>
    <script type="module" crossorigin src="/assets/index-BMu-j7Zi.js"></script>
    <link rel="stylesheet" crossorigin href="/assets/index-fneZqxTi.css">
  </head>
  <body>
    <div id="root"></div>

  </body>
</html>

```
# Style.css:
```
@import url("https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:ital,wght@1,500&display=swap");

:root {
  font-family: "DM Sans", "Helvetica Neue", sans-serif;
  color: #24251f;
  background: #f5f4ef;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  --paper: #f5f4ef;
  --ink: #24251f;
  --muted: #77786f;
  --line: #deddd5;
  --green: #546849;
  --serif: "Playfair Display", Georgia, serif;
  --mono: "DM Mono", "Courier New", monospace;
}

* {
  box-sizing: border-box;
}

html {
  min-width: 320px;
  scroll-behavior: smooth;
  scroll-padding-top: 92px;
}

body {
  margin: 0;
  min-width: 320px;
}

body::before {
  position: fixed;
  z-index: 5;
  inset: 0;
  pointer-events: none;
  content: "";
  opacity: 0.12;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.16'/%3E%3C/svg%3E");
}

a {
  color: inherit;
}

button,
a {
  -webkit-tap-highlight-color: transparent;
}

a:focus-visible,
button:focus-visible {
  outline: 2px solid var(--green);
  outline-offset: 5px;
}

.site-header {
  position: relative;
  z-index: 10;
  display: flex;
  width: min(100% - 112px, 1440px);
  height: 92px;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
  border-bottom: 1px solid var(--line);
}

.wordmark {
  color: var(--ink);
  font-size: 24px;
  font-weight: 700;
  letter-spacing: -2px;
  text-decoration: none;
}

.wordmark span {
  color: var(--green);
}

.navigation {
  display: flex;
  align-items: center;
  gap: clamp(24px, 4vw, 58px);
}

.navigation a,
.site-footer > a:last-child {
  font-size: 12px;
  font-weight: 500;
  text-decoration: none;
  transition: color 180ms ease;
}

.navigation a:hover,
.site-footer > a:last-child:hover {
  color: var(--green);
}

.navigation__contact,
.contact__links a {
  display: inline-flex;
  align-items: center;
  gap: 8px;
}

.arrow-icon {
  width: 18px;
  height: 18px;
  stroke: currentColor;
  stroke-linecap: round;
  stroke-linejoin: round;
  stroke-width: 1.4;
  transition: transform 180ms ease;
}

a:hover .arrow-icon {
  transform: translateX(3px);
}

.arrow-icon--diagonal {
  transform: rotate(-45deg);
}

a:hover .arrow-icon--diagonal {
  transform: translate(2px, -2px) rotate(-45deg);
}

.menu-toggle {
  display: none;
}

.page-shell,
.section-shell {
  width: min(100% - 112px, 1280px);
  margin: 0 auto;
}

.hero {
  display: grid;
  min-height: 700px;
  grid-template-columns: 1fr 0.88fr;
  align-items: center;
  gap: clamp(40px, 8vw, 130px);
  padding-top: 42px;
  padding-bottom: 70px;
}

.hero__copy {
  position: relative;
  padding: 18px 0 0 5.8%;
  animation: rise-in 760ms both;
}

.eyebrow,
.section-label,
.hero__index,
.portrait-caption,
.hero__side-note,
.about__foot,
.skill-row__number,
.recognition__year,
.contact__links,
.site-footer > span,
.site-footer > a:last-child {
  font-family: var(--mono);
  font-size: 9px;
  letter-spacing: 0.1em;
}

.eyebrow {
  display: flex;
  align-items: center;
  gap: 10px;
  margin: 0;
  color: var(--muted);
}

.status-dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #8d9f72;
  box-shadow: 0 0 0 4px rgb(141 159 114 / 15%);
}

h1,
h2,
p {
  margin-top: 0;
}

.hero h1 {
  margin: 29px 0 22px;
  font-size: clamp(68px, 8.5vw, 122px);
  font-weight: 500;
  letter-spacing: -0.085em;
  line-height: 0.91;
}

.hero__period {
  color: var(--green);
}

.hero__serif,
.serif-accent {
  color: var(--green);
  font-family: var(--serif);
  font-weight: 500;
  font-style: italic;
  letter-spacing: -0.07em;
}

.hero__intro {
  max-width: 390px;
  margin-bottom: 21px;
  color: #6b6c63;
  font-size: 14px;
  line-height: 1.8;
}

.hero__intro strong {
  color: var(--ink);
  font-weight: 600;
}

.text-link {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding-bottom: 5px;
  border-bottom: 1px solid #aeb3a4;
  font-size: 12px;
  font-weight: 600;
  text-decoration: none;
}

.hero__index {
  display: flex;
  align-items: center;
  gap: 11px;
  margin-top: 66px;
  color: #888980;
  font-size: 8px;
}

.hero__index span:first-child {
  color: var(--green);
}

.hero__index-line {
  width: 39px;
  height: 1px;
  background: #b7b7ad;
}

.hero__visual {
  position: relative;
  justify-self: center;
  width: min(100%, 410px);
  padding: 0 22px 23px 0;
  animation: rise-in 900ms 100ms both;
}

.portrait-frame {
  position: relative;
  width: 100%;
  height: clamp(430px, 48vw, 590px);
  overflow: hidden;
  background: #d7d9d1;
}

.portrait-frame::after {
  position: absolute;
  inset: 40% 0 0;
  content: "";
  background: linear-gradient(transparent, rgb(18 22 17 / 55%));
  pointer-events: none;
}

.portrait {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center 38%;
  display: block;
  transition: transform 700ms cubic-bezier(0.2, 0.7, 0.2, 1);
}

.portrait-frame:hover .portrait {
  transform: scale(1.035);
}

.portrait-caption {
  position: absolute;
  z-index: 1;
  right: 23px;
  bottom: 20px;
  left: 23px;
  display: flex;
  justify-content: space-between;
  gap: 10px;
  color: white;
  font-size: 8px;
}

.hero__visual::after {
  position: absolute;
  z-index: -1;
  right: 0;
  bottom: 0;
  width: 76%;
  height: 80%;
  border: 1px solid #c8c9bd;
  content: "";
}

.orbit-note {
  position: absolute;
  z-index: 2;
  top: 39px;
  right: -39px;
  display: flex;
  width: 91px;
  height: 91px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: 1px solid rgb(245 244 239 / 55%);
  border-radius: 50%;
  background: var(--paper);
  color: var(--green);
  font-family: var(--mono);
  font-size: 7px;
  letter-spacing: 0.08em;
  line-height: 1.55;
  text-align: center;
  transform: rotate(9deg);
}

.orbit-note__star {
  margin-bottom: 3px;
  font-size: 20px;
  line-height: 1;
}

.hero__side-note {
  position: absolute;
  top: 43%;
  right: -53px;
  color: #92938a;
  font-size: 7px;
  writing-mode: vertical-rl;
}

.marquee {
  overflow: hidden;
  padding: 19px 0;
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
}

.marquee__track {
  display: flex;
  width: max-content;
  animation: marquee 36s linear infinite;
}

.marquee__group {
  display: flex;
  align-items: center;
  gap: 28px;
  padding-right: 28px;
  color: #707167;
  font-family: var(--mono);
  font-size: 10px;
  letter-spacing: 0.16em;
}

.marquee__group i {
  color: #899779;
  font-size: 13px;
  font-style: normal;
}

.section-shell {
  padding-top: 113px;
  padding-bottom: 112px;
}

.section-label {
  display: flex;
  justify-content: space-between;
  padding-bottom: 13px;
  border-bottom: 1px solid var(--line);
  color: #83847a;
  font-size: 8px;
}

.section-label span:first-child {
  color: var(--green);
}

.about__grid {
  display: grid;
  grid-template-columns: 1.05fr 0.7fr;
  gap: 10%;
  padding: 78px 5.8% 69px;
}

.about h2,
.skills h2,
.recognition h2,
.contact h2 {
  margin: 0;
  font-size: clamp(48px, 6.4vw, 82px);
  font-weight: 500;
  letter-spacing: -0.075em;
  line-height: 1.02;
}

.about__body {
  max-width: 440px;
  padding-top: 9px;
}

.about__body p {
  color: #72736a;
  font-size: 13px;
  line-height: 1.9;
}

.about__body .about__lead {
  color: var(--ink);
  font-size: 17px;
  line-height: 1.65;
}

.about__body .text-link {
  margin-top: 7px;
}

.about__foot {
  display: flex;
  justify-content: space-between;
  padding: 16px 5.8% 0;
  border-top: 1px solid var(--line);
  color: #85867d;
  font-size: 8px;
}

.skills {
  padding-top: 0;
}

.skills__grid {
  display: grid;
  grid-template-columns: 0.8fr 1fr;
  gap: 12%;
  padding: 73px 5.8% 0;
}

.skills__intro {
  max-width: 270px;
  margin-top: 23px;
  color: #72736a;
  font-size: 12px;
  line-height: 1.85;
}

.skill-list {
  border-top: 1px solid var(--line);
}

.skill-row {
  display: grid;
  min-height: 57px;
  grid-template-columns: 42px 1fr 24px;
  align-items: center;
  border-bottom: 1px solid var(--line);
}

.skill-row__number {
  color: #98998f;
  font-size: 8px;
}

.skill-row__name {
  font-size: 14px;
  transition: color 180ms ease, transform 180ms ease;
}

.skill-row:hover .skill-row__name {
  color: var(--green);
  transform: translateX(5px);
}

.skill-row__mark {
  color: #a0a195;
  font-size: 13px;
}

.recognition {
  padding-top: 0;
}

.recognition__card {
  position: relative;
  display: grid;
  min-height: 336px;
  grid-template-columns: 130px 1fr auto;
  align-items: center;
  gap: 5%;
  margin-top: 37px;
  padding: 48px 6%;
  overflow: hidden;
  background: #e9e9df;
}

.recognition__card::before {
  position: absolute;
  top: -190px;
  right: 75px;
  width: 360px;
  height: 360px;
  border: 1px solid rgb(84 104 73 / 15%);
  border-radius: 50%;
  content: "";
}

.recognition__card::after {
  position: absolute;
  top: -140px;
  right: 125px;
  width: 260px;
  height: 260px;
  border: 1px solid rgb(84 104 73 / 15%);
  border-radius: 50%;
  content: "";
}

.recognition__badge {
  z-index: 1;
  display: grid;
  width: 92px;
  height: 92px;
  place-items: center;
  border: 1px solid #b2b9a8;
  border-radius: 50%;
  color: var(--green);
  font-size: 37px;
}

.recognition__copy {
  position: relative;
  z-index: 1;
  max-width: 500px;
}

.recognition__copy .eyebrow {
  margin-bottom: 22px;
}

.recognition h2 {
  font-size: clamp(39px, 5vw, 59px);
}

.recognition__copy > p:last-child {
  max-width: 430px;
  margin: 19px 0 0;
  color: #6d6f64;
  font-size: 12px;
  line-height: 1.85;
}

.recognition__year {
  position: relative;
  z-index: 1;
  align-self: end;
  margin-bottom: 8px;
  color: var(--green);
  font-size: 18px;
}

.recognition__year span {
  color: #85877c;
  font-size: 8px;
}

.contact {
  padding-top: 0;
  padding-bottom: 96px;
}

.contact__content {
  padding: 75px 5.8% 73px;
}

.contact__content .eyebrow {
  margin-bottom: 24px;
}

.contact h2 {
  font-size: clamp(54px, 8vw, 100px);
}

.contact__button {
  display: flex;
  width: fit-content;
  min-width: min(100%, 400px);
  align-items: center;
  justify-content: space-between;
  gap: 28px;
  margin-top: 34px;
  padding: 14px 0;
  border-bottom: 1px solid #afb2a7;
  font-size: 13px;
  text-decoration: none;
}

.contact__links {
  display: flex;
  gap: 28px;
  padding: 16px 5.8% 0;
  border-top: 1px solid var(--line);
  color: #74756b;
  font-size: 8px;
}

.contact__links a {
  text-decoration: none;
}

.contact__links .arrow-icon {
  width: 13px;
  height: 13px;
}

.site-footer {
  display: flex;
  min-height: 78px;
  width: min(100% - 112px, 1440px);
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
  border-top: 1px solid var(--line);
}

.site-footer > span,
.site-footer > a:last-child {
  color: #898a80;
  font-size: 8px;
  text-decoration: none;
}

@keyframes rise-in {
  from {
    opacity: 0;
    transform: translateY(18px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes marquee {
  to {
    transform: translateX(-50%);
  }
}

@media (min-width: 1500px) {
  .hero {
    min-height: 780px;
  }
}

@media (max-width: 900px) {
  .site-header,
  .page-shell,
  .section-shell,
  .site-footer {
    width: min(100% - 64px, 1280px);
  }

  .hero {
    min-height: 620px;
    grid-template-columns: 1fr 0.85fr;
    gap: 4%;
  }

  .hero__copy {
    padding-left: 0;
  }

  .hero h1 {
    font-size: clamp(65px, 9.5vw, 88px);
  }

  .portrait-frame {
    height: min(59vw, 530px);
  }

  .hero__side-note {
    right: -28px;
  }

  .orbit-note {
    right: -22px;
    width: 76px;
    height: 76px;
    font-size: 6px;
  }

  .about__grid,
  .skills__grid {
    padding-right: 0;
    padding-left: 0;
  }

  .recognition__card {
    grid-template-columns: 90px 1fr auto;
    gap: 4%;
    padding-right: 5%;
    padding-left: 5%;
  }

  .recognition__badge {
    width: 74px;
    height: 74px;
  }
}

@media (max-width: 640px) {
  html {
    scroll-padding-top: 72px;
  }

  .site-header,
  .page-shell,
  .section-shell,
  .site-footer {
    width: calc(100% - 40px);
  }

  .site-header {
    height: 72px;
  }

  .menu-toggle {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    padding: 8px 0 8px 8px;
    border: 0;
    background: transparent;
    color: var(--ink);
    font-family: var(--mono);
    font-size: 9px;
    letter-spacing: 0.08em;
  }

  .menu-toggle__icon {
    display: flex;
    width: 16px;
    flex-direction: column;
    gap: 5px;
  }

  .menu-toggle__icon i {
    width: 16px;
    height: 1px;
    background: var(--ink);
    transition: transform 180ms ease;
  }

  .menu-toggle__icon.is-open i:first-child {
    transform: translateY(3px) rotate(45deg);
  }

  .menu-toggle__icon.is-open i:last-child {
    transform: translateY(-3px) rotate(-45deg);
  }

  .navigation {
    position: absolute;
    top: 71px;
    right: -20px;
    left: -20px;
    display: none;
    flex-direction: column;
    align-items: stretch;
    gap: 0;
    padding: 10px 20px 20px;
    border-bottom: 1px solid var(--line);
    background: var(--paper);
  }

  .navigation--open {
    display: flex;
  }

  .navigation a {
    padding: 14px 0;
    border-bottom: 1px solid var(--line);
    font-size: 13px;
  }

  .navigation__contact {
    justify-content: space-between;
  }

  .hero {
    min-height: auto;
    grid-template-columns: 1fr;
    gap: 50px;
    padding-top: 58px;
    padding-bottom: 59px;
  }

  .hero__copy {
    padding-top: 0;
  }

  .hero h1 {
    margin-top: 25px;
    font-size: clamp(68px, 16vw, 96px);
  }

  .hero__intro {
    max-width: 360px;
    font-size: 13px;
  }

  .hero__index {
    margin-top: 36px;
  }

  .hero__visual {
    width: min(82%, 390px);
    padding-right: 14px;
    padding-bottom: 15px;
  }

  .portrait-frame {
    height: min(112vw, 500px);
  }

  .portrait {
    object-position: center 34%;
  }

  .portrait-caption {
    right: 14px;
    bottom: 14px;
    left: 14px;
    font-size: 6px;
  }

  .orbit-note {
    top: 27px;
    right: -26px;
  }

  .hero__side-note {
    right: -24px;
    font-size: 6px;
  }

  .marquee {
    padding: 16px 0;
  }

  .marquee__group {
    gap: 20px;
    padding-right: 20px;
    font-size: 9px;
  }

  .section-shell {
    padding-top: 78px;
    padding-bottom: 78px;
  }

  .section-label {
    font-size: 7px;
  }

  .section-label span:last-child {
    text-align: right;
  }

  .about__grid {
    grid-template-columns: 1fr;
    gap: 27px;
    padding: 47px 0;
  }

  .about h2,
  .skills h2 {
    font-size: clamp(58px, 14vw, 76px);
  }

  .about__body {
    padding-top: 0;
  }

  .about__body .about__lead {
    font-size: 16px;
  }

  .about__foot {
    gap: 16px;
    padding-right: 0;
    padding-left: 0;
    font-size: 7px;
  }

  .skills {
    padding-top: 0;
  }

  .skills__grid {
    grid-template-columns: 1fr;
    gap: 36px;
    padding-top: 46px;
  }

  .skills__intro {
    max-width: 320px;
    margin-top: 15px;
  }

  .recognition {
    padding-top: 0;
  }

  .recognition__card {
    grid-template-columns: 1fr auto;
    gap: 24px 12px;
    margin-top: 24px;
    padding: 34px 25px;
  }

  .recognition__badge {
    width: 60px;
    height: 60px;
    font-size: 27px;
  }

  .recognition__copy {
    grid-column: 1 / -1;
    grid-row: 2;
  }

  .recognition__copy .eyebrow {
    font-size: 7px;
    line-height: 1.7;
  }

  .recognition h2 {
    font-size: clamp(39px, 11vw, 53px);
  }

  .recognition__year {
    justify-self: end;
    align-self: center;
    margin: 0;
  }

  .recognition__card::before {
    right: -200px;
  }

  .recognition__card::after {
    right: -150px;
  }

  .contact {
    padding-top: 0;
    padding-bottom: 69px;
  }

  .contact__content {
    padding: 48px 0;
  }

  .contact__content .eyebrow {
    max-width: 280px;
    font-size: 7px;
    line-height: 1.7;
  }

  .contact h2 {
    font-size: clamp(51px, 12.5vw, 78px);
  }

  .contact__button {
    min-width: 0;
    width: 100%;
    gap: 12px;
    font-size: 11px;
  }

  .contact__links {
    padding-right: 0;
    padding-left: 0;
  }

  .site-footer {
    min-height: 70px;
  }

  .site-footer > span {
    max-width: 120px;
    font-size: 6px;
    line-height: 1.6;
    text-align: center;
  }

  .site-footer > a:last-child {
    font-size: 7px;
  }
}

@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    scroll-behavior: auto !important;
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}

```
## OUTPUT
<img width="1917" height="1100" alt="image" src="https://github.com/user-attachments/assets/16518d48-7bf0-41eb-96d2-3296179dffa1" />

<img width="1895" height="981" alt="image" src="https://github.com/user-attachments/assets/cf26e206-5573-4388-9147-2b149711e4a1" />

<img width="1907" height="982" alt="image" src="https://github.com/user-attachments/assets/ae9b80be-7077-4167-9db4-b473553c9a81" />

<img width="1897" height="1087" alt="image" src="https://github.com/user-attachments/assets/4b1bcbe7-8a15-4895-bfaa-28ecf51a4bf2" />


## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
