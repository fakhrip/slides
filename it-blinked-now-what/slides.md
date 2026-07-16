---
theme: seriph
title: It Blinked. Now What?
info: How day-to-day embedded software and hardware work turns an idea into a product people pay for.
class: text-white
transition: slide-left
mdc: true
fonts:
  sans: Inter
  serif: Fraunces
  mono: JetBrains Mono
css: unocss
---

<style global>
:root {
  --bg: #0b0d10;
  --panel: rgba(14, 17, 21, 0.78);
  --panel-strong: rgba(10, 12, 15, 0.88);
  --line: rgba(255, 255, 255, 0.12);
  --teal: #62f5ee;
  --amber: #ffb84a;
  --text: #f5f7fa;
  --muted: #b8c0cc;
}

.slidev-layout {
  padding: 0 !important;
  background:
    radial-gradient(circle at 16% 15%, rgba(98, 245, 238, 0.07), transparent 26%),
    radial-gradient(circle at 83% 14%, rgba(255, 184, 74, 0.06), transparent 24%),
    linear-gradient(180deg, #0d1014 0%, #080a0d 100%) !important;
  color: var(--text);
  font-family: Inter, ui-sans-serif, system-ui;
}

.slidev-layout h1,
.slidev-layout h2,
.slidev-layout h3,
.slidev-layout p,
.slidev-layout ul,
.slidev-layout li {
  margin: 0;
}

.kSlide {
  position: absolute;
  inset: 0;
  padding: 3.8rem 4.5rem;
  overflow: hidden;
}

.kTextPanel {
  position: absolute;
  z-index: 2;
  left: 4.5rem;
  top: 50%;
  transform: translateY(-50%);
  width: calc(56% - 5.5rem);
  max-height: calc(100% - 7rem);
  overflow: hidden;
  padding: 1.9rem 2rem;
  border-radius: 1.55rem;
  border: 1px solid var(--line);
  background: rgba(10, 13, 17, 0.72);
  box-shadow: 0 24px 80px rgba(0,0,0,0.28);
  backdrop-filter: blur(16px);
}

.kMediaPanel {
  position: absolute;
  z-index: 1;
  right: 4.5rem;
  top: 50%;
  transform: translateY(-50%);
  width: calc(44% - 3.5rem);
  height: min(72vh, 34rem);
  display: flex;
  align-items: center;
  justify-content: center;
}

.kMediaPanel.left {
  left: 4.5rem;
  right: auto;
}

.kTextPanel.right {
  right: 4.5rem;
  left: auto;
}

.kCopyBox,
.kCopyPlain {
  max-width: none;
}

.kHeroBox {
  position: relative;
  z-index: 2;
  width: min(54rem, calc(100vw - 8rem));
  margin: 0 auto;
  padding: 2.7rem 3.1rem;
  text-align: center;
  border-radius: 2rem;
  border: 1px solid rgba(255, 255, 255, 0.13);
  background: rgba(8, 10, 13, 0.76);
  box-shadow: 0 28px 90px rgba(0, 0, 0, 0.34);
  backdrop-filter: blur(18px);
}

.kEyebrow {
  color: var(--teal);
  text-transform: uppercase;
  letter-spacing: 0.22em;
  font-size: 0.72rem;
  font-weight: 800;
}

.kHeroTitle {
  margin-top: 0.75rem !important;
  color: var(--text);
  font-size: clamp(4rem, 8vw, 6.2rem);
  line-height: 0.94;
  letter-spacing: -0.055em;
  font-weight: 820;
}

.kTitle {
  margin-top: 0.72rem !important;
  color: var(--text);
  font-size: clamp(2.1rem, 3.2vw, 3.15rem);
  line-height: 1.02;
  letter-spacing: -0.042em;
  font-weight: 800;
  max-width: 12.5em;
}

.kSubtitle,
.kBody {
  color: var(--muted);
  line-height: 1.48;
}

.kSubtitle {
  max-width: 34rem;
  margin: 1.25rem auto 0 !important;
  font-size: 1.12rem;
}

.kBody {
  max-width: 34rem;
  margin-top: 1rem !important;
  font-size: 1rem;
}

.kBullets {
  margin-top: 1.2rem !important;
  padding-left: 1.1rem;
  display: grid;
  gap: 0.48rem;
  color: var(--muted);
  font-size: 0.88rem;
  line-height: 1.36;
}

.kBullets strong,
.kCard strong,
.kStep strong {
  color: var(--text);
  font-weight: 800;
}

.kImageFrame {
  width: 100%;
  height: 100%;
  border-radius: 1.6rem;
  border: 1px solid rgba(255,255,255,0.11);
  background: rgba(255,255,255,0.025);
  overflow: hidden;
  box-shadow: 0 28px 90px rgba(0,0,0,0.32);
}

.kImageFrame img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: contain;
  object-position: center;
}

.kHeroVisual {
  position: absolute;
  z-index: 1;
  left: 50%;
  right: 5rem;
  bottom: 2.7rem;
  top: 50%;
  opacity: 0.62;
}

.kHeroVisual img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  object-position: center;
}

.kGlow {
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 72% 68%, rgba(98,245,238,0.12), transparent 30%), radial-gradient(circle at 68% 40%, rgba(255,184,74,0.08), transparent 28%);
  pointer-events: none;
}

.kGrid2 {
  margin-top: 1.15rem !important;
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 0.75rem;
}

.kGrid3 {
  margin-top: 1.15rem !important;
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.75rem;
}

.kCard,
.kStep {
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: 1.1rem;
  background: rgba(16,19,23,0.62);
  padding: 0.72rem 0.82rem;
}

.kCard span,
.kStep span {
  display: block;
  margin-top: 0.25rem;
  color: var(--muted);
  font-size: 0.82rem;
  line-height: 1.32;
}

.kTerm {
  margin-top: 1.1rem !important;
  padding-top: 0.72rem;
  border-top: 1px solid rgba(255,255,255,0.09);
  color: rgba(245,247,250,0.62);
  font-size: 0.76rem;
  line-height: 1.35;
}

.kClosing {
  position: relative;
  z-index: 2;
  width: min(62rem, calc(100vw - 8rem));
  margin: 0 auto;
  text-align: center;
}
</style>

<div class="kSlide flex items-center justify-center">
<div class="kGlow"></div>
<div class="kHeroVisual">
<img src="/cover-product-journey.png" alt="product journey illustration" />
</div>
<div class="kHeroBox">
<div class="kEyebrow">embedded systems · product · business</div>
<h1 class="kHeroTitle">It Blinked.<br>Now What?</h1>
<p class="kSubtitle">How embedded software and hardware work becomes a product people understand, trust, and pay for.</p>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel">
<div class="kEyebrow">the real journey</div>
<h1 class="kTitle">A blinking LED is not a business.</h1>
<p class="kBody">The first prototype proves that something <em>can</em> work. The product journey proves that it can survive customers, manufacturing, support, and sales.</p>
<ul class="kBullets">
<li><strong>Prototype:</strong> prove the riskiest technical assumption.</li>
<li><strong>Product:</strong> make it reliable, repeatable, supportable, and cost-aware.</li>
<li><strong>Business:</strong> connect the work to pricing, deployment, and customer value.</li>
<li><strong>Outcome:</strong> move from “it works” to “people buy and keep using it.”</li>
</ul>
</div>
<div class="kMediaPanel">
<div class="kImageFrame">
<img src="/blinking-led-not-business.png" alt="journey from product concept to customer outcome" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel right">
<div class="kEyebrow">disclaimer</div>
<h1 class="kTitle">This is about building a business, not pure research.</h1>
<p class="kBody">The question is not only “Can we build it?” The bigger question is “Can this solve a painful problem, reliably, at a price someone accepts?”</p>
<div class="kGrid2">
<div class="kCard"><strong>Included</strong><span>Product thinking, customer discovery, MVPs, PMF, sales, and scaling risk.</span></div>
<div class="kCard"><strong>Not the focus</strong><span>Publication-first work, lab-only exploration, or novelty without a user path.</span></div>
<div class="kCard"><strong>Still important</strong><span>Research matters when it closes gaps the business cannot ignore.</span></div>
<div class="kCard"><strong>Mindset</strong><span>Think customer, economics, operations, and support—not just clever engineering.</span></div>
</div>
</div>
<div class="kMediaPanel left">
<div class="kImageFrame">
<img src="/research-reduces-risk.png" alt="research streams reducing risk" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel">
<div class="kEyebrow">from demo to product</div>
<h1 class="kTitle">Arduino is a great start. It is usually not enough.</h1>
<p class="kBody">Dev boards are useful for fast learning and PoCs. Production adds constraints that prototypes often hide.</p>
<ul class="kBullets">
<li><strong>Electrical reality:</strong> power, thermal behavior, signal integrity, EMI, and EMC.</li>
<li><strong>Device reality:</strong> boot, update, rollback, diagnostics, and recovery.</li>
<li><strong>Manufacturing reality:</strong> BOM, assembly time, test jigs, enclosure, and yield.</li>
<li><strong>Market reality:</strong> support, warranty, safety, certification, and lifecycle cost.</li>
</ul>
</div>
<div class="kMediaPanel">
<div class="kImageFrame">
<img src="/beyond-arduino.png" alt="progression from dev board to custom product" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel right">
<div class="kEyebrow">go deeper</div>
<h1 class="kTitle">Embedded products are built on layers of deep expertise.</h1>
<p class="kBody">Expertise can sit at the lowest level, the hardware level, the firmware level, the system level, or the product level. In embedded systems, every layer leaks eventually.</p>
<ul class="kBullets">
<li><strong>Lowest level:</strong> silicon, FPGA, chip design, timing, and verification.</li>
<li><strong>Hardware level:</strong> electronics, PCB, RF, power, sensors, enclosure, CNC, DFM, and DFT.</li>
<li><strong>Firmware level:</strong> bootloaders, drivers, RTOS, protocol stacks, OTA, and diagnostics.</li>
<li><strong>System level:</strong> kernel, OS, networking, security, observability, and fleet operations.</li>
<li><strong>Product level:</strong> customer workflow, onboarding, pricing, support, and sales.</li>
</ul>
<p class="kTerm">FPGA = Field-Programmable Gate Array · PCB = Printed Circuit Board · CNC = Computer Numerical Control · DFM/DFT = Design for Manufacturing / Design for Test · RTOS = Real-Time Operating System · OTA = Over-the-Air update.</p>
</div>
<div class="kMediaPanel left">
<div class="kImageFrame">
<img src="/expertise-stack.png" alt="stack from silicon to product" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel">
<div class="kEyebrow">customer first</div>
<h1 class="kTitle">Start with customer pain—not components.</h1>
<p class="kBody">Customers do not care how elegant the board is. They care whether the product makes an important problem cheaper, faster, safer, easier, or measurable.</p>
<div class="kGrid2">
<div class="kCard"><strong>Who hurts?</strong><span>Which user, team, or operator feels the pain directly?</span></div>
<div class="kCard"><strong>How often?</strong><span>Is the problem frequent enough to justify behavior change and budget?</span></div>
<div class="kCard"><strong>What happens now?</strong><span>Understand the current workaround before pitching your improvement.</span></div>
<div class="kCard"><strong>Why switch?</strong><span>There must be enough value to overcome friction, risk, and retraining.</span></div>
</div>
</div>
<div class="kMediaPanel">
<div class="kImageFrame">
<img src="/customer-pain-to-outcome.png" alt="customer problem to product outcome" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel">
<div class="kEyebrow">why research matters</div>
<h1 class="kTitle">Research fills gaps the business cannot afford to ignore.</h1>
<p class="kBody">Good research turns unknowns into evidence. For an embedded business, that means reducing technical, market, manufacturing, and compliance risk before those risks become expensive.</p>
<ul class="kBullets">
<li><strong>Market research:</strong> is the pain real, urgent, and budget-worthy?</li>
<li><strong>Customer interviews:</strong> what does “good enough” actually mean?</li>
<li><strong>Technical validation:</strong> will the design work outside the lab?</li>
<li><strong>Compliance review:</strong> what standards, emissions, or safety rules apply?</li>
<li><strong>Manufacturing research:</strong> can this be built repeatedly at the target cost?</li>
</ul>
</div>
<div class="kMediaPanel">
<div class="kImageFrame">
<img src="/research-reduces-risk.png" alt="research reducing risk and increasing confidence" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel right">
<div class="kEyebrow">core product journey</div>
<h1 class="kTitle">PoC, MVP, PMF, and Sales answer different questions.</h1>
<div class="kGrid2">
<div class="kStep"><strong>PoC — Proof of Concept</strong><span>Can the riskiest thing work at all?</span></div>
<div class="kStep"><strong>MVP — Minimum Viable Product</strong><span>What is the smallest complete learning loop we can test with real users?</span></div>
<div class="kStep"><strong>PMF — Product-Market Fit</strong><span>Do customers keep pulling because the value is strong enough?</span></div>
<div class="kStep"><strong>Sales</strong><span>Can buying, deployment, and support become repeatable and profitable?</span></div>
</div>
<p class="kTerm">MVP = Minimum Viable Product · PMF = Product-Market Fit.</p>
</div>
<div class="kMediaPanel left">
<div class="kImageFrame">
<img src="/poc-mvp-pmf-sales.png" alt="PoC to sales journey" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel">
<div class="kEyebrow">day-to-day engineering work</div>
<h1 class="kTitle">What engineers actually do across the journey.</h1>
<div class="kGrid2">
<div class="kCard"><strong>Idea</strong><span>Problem discovery, sketches, architecture trade-offs, early feasibility, and rough BOM thinking.</span></div>
<div class="kCard"><strong>PoC</strong><span>Dev boards, firmware spikes, signal capture, mechanical mockups, and risky integrations.</span></div>
<div class="kCard"><strong>MVP</strong><span>Custom PCB rev A, enclosure, test fixtures, OTA, logs, and pilot installation flow.</span></div>
<div class="kCard"><strong>PMF</strong><span>Reliability hardening, manufacturing process, support tooling, analytics, and onboarding.</span></div>
<div class="kCard"><strong>Sales</strong><span>Demos, procurement answers, rollout planning, maintenance promises, and roadmap trade-offs.</span></div>
<div class="kCard"><strong>Always</strong><span>Documentation, debugging, testing, customer feedback, and cost pressure from reality.</span></div>
</div>
<p class="kTerm">BOM = Bill of Materials · PCB = Printed Circuit Board · OTA = Over-the-Air update.</p>
</div>
<div class="kMediaPanel">
<div class="kImageFrame">
<img src="/cover-product-journey.png" alt="product development roadmap" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel">
<div class="kEyebrow">real example journey</div>
<h1 class="kTitle">Example: smart sensor / IoT device.</h1>
<p class="kBody">Imagine a maintenance team that notices machine issues too late. The opportunity is not “a cool sensor.” The opportunity is earlier detection, lower downtime, and better planning.</p>
<ul class="kBullets">
<li><strong>Idea:</strong> identify a maintenance problem with real operational cost.</li>
<li><strong>PoC:</strong> prove useful signals such as vibration or temperature can be captured.</li>
<li><strong>MVP:</strong> create a pilot device with custom hardware, rugged enclosure, dashboard, and install guide.</li>
<li><strong>PMF:</strong> customers ask for more units, more sites, and tighter integration.</li>
<li><strong>Sales:</strong> sell the device, deployment, dashboard, and support motion.</li>
</ul>
<p class="kTerm">IoT = Internet of Things.</p>
</div>
<div class="kMediaPanel">
<div class="kImageFrame">
<img src="/smart-sensor-iot-example.png" alt="smart sensor and dashboard example" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel right">
<div class="kEyebrow">business mechanics</div>
<h1 class="kTitle">Unit economics: hardware must pay for itself.</h1>
<p class="kBody">Pricing is not only “cost plus margin.” Hardware pricing has to survive manufacturing, warranty, support, sales, and future revisions.</p>
<ul class="kBullets">
<li><strong>COGS — Cost of Goods Sold:</strong> direct cost to build and deliver one unit.</li>
<li><strong>BOM:</strong> parts and components inside that unit cost.</li>
<li><strong>Hidden costs:</strong> returns, installation, warranty, support, failed batches, and field replacements.</li>
<li><strong>Recurring revenue:</strong> subscriptions, premium support, service contracts, or software.</li>
<li><strong>Gross margin:</strong> what remains after unit cost, before operating expenses.</li>
</ul>
<p class="kTerm">COGS = Cost of Goods Sold · BOM = Bill of Materials · Gross margin = selling price minus direct unit cost.</p>
</div>
<div class="kMediaPanel left">
<div class="kImageFrame">
<img src="/unit-economics.png" alt="hardware unit economics flowchart" />
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="kSlide">
<div class="kTextPanel">
<div class="kEyebrow">what comes next</div>
<h1 class="kTitle">After MVP, the job becomes validation to scale.</h1>
<p class="kBody">This is where engineering validation, design validation, production validation, certification, and mass production enter the picture. Each deserves its own deep dive.</p>
<ul class="kBullets">
<li><strong>EVT — Engineering Validation Test:</strong> prove that the core engineering works.</li>
<li><strong>DVT — Design Validation Test:</strong> prove that the design is stable, usable, and robust.</li>
<li><strong>PVT — Production Validation Test:</strong> prove that the factory can build it repeatedly.</li>
<li><strong>Certification:</strong> FCC, CE, EMC, and safety often determine market access and schedule risk.</li>
<li><strong>Mass production:</strong> focus on yield, QA, suppliers, support, and operational repeatability.</li>
</ul>
<p class="kTerm">FCC = U.S. communications and emissions compliance · CE = European conformity marking · EMC = Electromagnetic Compatibility · QA = Quality Assurance.</p>
</div>
<div class="kMediaPanel">
<div class="kImageFrame">
<img src="/after-mvp-roadmap.png" alt="after MVP roadmap" />
</div>
</div>
</div>

---
layout: center
class: text-white
---

<div class="kSlide flex items-center justify-center">
<div class="kGlow"></div>
<div class="kClosing">
<div class="kEyebrow">final thought</div>
<h1 class="kHeroTitle">The blink is the beginning.</h1>
<p class="kSubtitle">The real product is everything after that: customer pain, deep engineering, validation, manufacturing, useful software, clear economics, and repeatable sales.</p>
<div class="kImageFrame mt-10 mx-auto" style="max-width: 34rem;">
<img src="/cover-product-journey.png" alt="product development journey" />
</div>
</div>
</div>
