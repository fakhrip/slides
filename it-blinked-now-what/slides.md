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

<div class="absolute inset-0 flex justify-center px-16 py-7">
<div class="relative h-full w-full max-w-240">
<div class="absolute left-1/2 top-2 z-0 h-[23rem] w-[52rem] -translate-x-1/2 overflow-hidden rounded-3xl border border-white/10 bg-white/3 shadow-2xl">
<img
  src="/cover-product-journey.png"
  alt="Embedded product journey"
  class="h-full w-full object-cover object-center"
/>
<div class="absolute inset-0 bg-gradient-to-b from-black/0 via-black/0 to-black/18"></div>
</div>

<div class="absolute left-1/2 top-[19rem] z-10 w-full max-w-[50rem] -translate-x-1/2 rounded-3xl border border-white/12 bg-[#090d10]/94 px-7 py-6 shadow-2xl backdrop-blur-xl">
<div class="grid grid-cols-[0.9fr_1.1fr] items-center gap-6">
<div class="text-center">
<h1 class="m-0 text-[2.45rem] font-800 leading-[0.98] tracking-[-0.05em] text-white">
It Blinked<br>
Now What?
</h1>
</div>

<div class="rounded-2xl border border-white/10 bg-white/4 px-5 py-4 text-left">
<p class="m-0 text-[0.78rem] leading-[1.55] text-white/62">
How embedded software and hardware work becomes a product people understand, trust, and pay for.
</p>
</div>
</div>
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel">
<div class="k-eyebrow">the real journey</div>
<h1 class="k-title">A blinking LED is not a business.</h1>
<p class="k-body">The first prototype proves that something <em>can</em> work. The product journey proves that it can survive customers, manufacturing, support, and sales.</p>

<div class="k-grid2">
<div class="k-card">
<strong>Prototype</strong>
<span>Prove the riskiest technical assumption.</span>
</div>

<div class="k-card">
<strong>Product</strong>
<span>Make it reliable, repeatable, supportable, and cost-aware.</span>
</div>

<div class="k-card">
<strong>Business</strong>
<span>Connect engineering to pricing, deployment, and customer value.</span>
</div>

<div class="k-card">
<strong>Outcome</strong>
<span>Move from “it works” to people buy and keep using it.</span>
</div>
</div>
</div>

<div class="k-media-panel">
<img src="/blinking-led-not-business.png" alt="journey from product concept to customer outcome" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel k-right">
<div class="k-eyebrow">disclaimer</div>
<h1 class="k-title">This is about building a business, not pure research.</h1>
<p class="k-body">The question is not only “Can we build it?” The bigger question is “Can this solve a painful problem, reliably, at a price someone accepts?”</p>

<div class="k-grid2">
<div class="k-card">
<strong>Included</strong>
<span>Product thinking, customer discovery, MVPs, PMF, sales, and scaling risk.</span>
</div>

<div class="k-card">
<strong>Not the focus</strong>
<span>Publication-first work, lab-only exploration, or novelty without a user path.</span>
</div>

<div class="k-card">
<strong>Still important</strong>
<span>Research matters when it closes gaps the business cannot ignore.</span>
</div>

<div class="k-card">
<strong>Mindset</strong>
<span>Think customer, economics, operations, and support—not just clever engineering.</span>
</div>
</div>
</div>

<div class="k-media-panel k-left">
<img src="/research-reduces-risk.png" alt="research streams reducing risk" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel">
<div class="k-eyebrow">from demo to product</div>
<h1 class="k-title">Arduino is a great start. It is usually not enough.</h1>
<p class="k-body">Dev boards are useful for fast learning and PoCs. Production adds constraints that prototypes often hide.</p>

<ul class="k-bullets">
<li><strong>Electrical reality:</strong> power, thermal behavior, signal integrity, EMI, and EMC.</li>
<li><strong>Device reality:</strong> boot, update, rollback, diagnostics, and recovery.</li>
<li><strong>Manufacturing reality:</strong> BOM, assembly time, test jigs, enclosure, and yield.</li>
<li><strong>Market reality:</strong> support, warranty, safety, certification, and lifecycle cost.</li>
</ul>
</div>

<div class="k-media-panel">
<img src="/beyond-arduino.png" alt="progression from dev board to custom product" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel k-right">
<div class="k-eyebrow">go deeper</div>
<h1 class="k-title">Embedded products are built on layers of deep expertise.</h1>
<p class="k-body">Expertise can sit at the lowest level, hardware, firmware, system, or product level. In embedded systems, every layer leaks eventually.</p>

<ul class="k-bullets">
<li><strong>Lowest:</strong> silicon, FPGA, chip design, timing, and verification.</li>
<li><strong>Hardware:</strong> electronics, PCB, RF, power, sensors, enclosure, CNC, DFM, and DFT.</li>
<li><strong>Firmware:</strong> bootloaders, drivers, RTOS, protocol stacks, OTA, and diagnostics.</li>
<li><strong>System:</strong> kernel, OS, networking, security, observability, and fleet operations.</li>
<li><strong>Product:</strong> workflow, onboarding, pricing, support, and sales.</li>
</ul>

<p class="k-term">FPGA = Field-Programmable Gate Array · PCB = Printed Circuit Board · CNC = Computer Numerical Control · DFM/DFT = Design for Manufacturing / Design for Test · RTOS = Real-Time Operating System · OTA = Over-the-Air update.</p>
</div>

<div class="k-media-panel k-left">
<img src="/expertise-stack.png" alt="stack from silicon to product" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel">
<div class="k-eyebrow">customer first</div>
<h1 class="k-title">Start with customer pain—not components.</h1>
<p class="k-body">Customers do not care how elegant the board is. They care whether the product makes an important problem cheaper, faster, safer, easier, or measurable.</p>

<div class="k-grid2">
<div class="k-card">
<strong>Who hurts?</strong>
<span>Which user, team, or operator feels the pain directly?</span>
</div>

<div class="k-card">
<strong>How often?</strong>
<span>Is the problem frequent enough to justify behavior change?</span>
</div>

<div class="k-card">
<strong>What happens now?</strong>
<span>Understand the current workaround before pitching.</span>
</div>

<div class="k-card">
<strong>Why switch?</strong>
<span>There must be enough value to beat friction and risk.</span>
</div>
</div>
</div>

<div class="k-media-panel">
<img src="/customer-pain-to-outcome.png" alt="customer problem to product outcome" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel k-right">
<div class="k-eyebrow">why research matters</div>
<h1 class="k-title">Research fills gaps the business cannot afford to ignore.</h1>
<p class="k-body">Good research turns unknowns into evidence before technical, market, manufacturing, and compliance risks become expensive.</p>

<ul class="k-bullets">
<li><strong>Market research:</strong> is the pain real, urgent, and budget-worthy?</li>
<li><strong>Customer interviews:</strong> what does “good enough” mean?</li>
<li><strong>Technical validation:</strong> will the design work outside the lab?</li>
<li><strong>Compliance review:</strong> what emissions or safety rules apply?</li>
<li><strong>Manufacturing research:</strong> can this be built repeatedly at target cost?</li>
</ul>
</div>

<div class="k-media-panel k-left">
<img src="/research-reduces-risk.png" alt="research reducing risk and increasing confidence" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel">
<div class="k-eyebrow">core product journey</div>
<h1 class="k-title">PoC, MVP, PMF, and Sales answer different questions.</h1>

<div class="k-grid2">
<div class="k-step">
<strong>PoC</strong>
<span>Can the riskiest thing work at all?</span>
</div>

<div class="k-step">
<strong>MVP</strong>
<span>What is the smallest complete learning loop?</span>
</div>

<div class="k-step">
<strong>PMF</strong>
<span>Do customers keep pulling because value is strong?</span>
</div>

<div class="k-step">
<strong>Sales</strong>
<span>Can buying, deployment, and support repeat profitably?</span>
</div>
</div>

<p class="k-term">PoC = Proof of Concept · MVP = Minimum Viable Product · PMF = Product-Market Fit.</p>
</div>

<div class="k-media-panel">
<img src="/poc-mvp-pmf-sales.png" alt="PoC to sales journey" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel k-right">
<div class="k-eyebrow">day-to-day work</div>
<h1 class="k-title">What engineers actually do across the journey.</h1>

<div class="k-grid2">
<div class="k-card">
<strong>Idea</strong>
<span>Problem discovery, sketches, trade-offs, feasibility, rough BOM.</span>
</div>

<div class="k-card">
<strong>PoC</strong>
<span>Dev boards, firmware spikes, signal capture, mockups.</span>
</div>

<div class="k-card">
<strong>MVP</strong>
<span>Custom PCB rev A, enclosure, fixtures, OTA, logs.</span>
</div>

<div class="k-card">
<strong>PMF</strong>
<span>Reliability, manufacturing process, support tooling, analytics.</span>
</div>

<div class="k-card">
<strong>Sales</strong>
<span>Demos, procurement answers, rollout and maintenance plans.</span>
</div>

<div class="k-card">
<strong>Always</strong>
<span>Documentation, debugging, testing, feedback, cost pressure.</span>
</div>
</div>

<p class="k-term">BOM = Bill of Materials · PCB = Printed Circuit Board · OTA = Over-the-Air update.</p>
</div>

<div class="k-media-panel k-left">
<img src="/cover-product-journey.png" alt="product development roadmap" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel">
<div class="k-eyebrow">real example journey</div>
<h1 class="k-title">Example: smart sensor / IoT device.</h1>
<p class="k-body">The opportunity is not “a cool sensor.” The opportunity is earlier detection, lower downtime, and better planning.</p>

<div class="k-grid2">
<div class="k-card">
<strong>Idea</strong>
<span>Find a maintenance problem with real operational cost.</span>
</div>

<div class="k-card">
<strong>PoC</strong>
<span>Prove useful vibration or temperature signals can be captured.</span>
</div>

<div class="k-card">
<strong>MVP</strong>
<span>Build pilot hardware, enclosure, dashboard, and install guide.</span>
</div>

<div class="k-card">
<strong>PMF</strong>
<span>Customers ask for more units, sites, and integrations.</span>
</div>

<div class="k-card k-wide k-accent">
<strong>Sales</strong>
<span>Sell the device, deployment, dashboard, and support.</span>
</div>
</div>

<p class="k-term">IoT = Internet of Things.</p>
</div>

<div class="k-media-panel">
<img src="/smart-sensor-iot-example.png" alt="smart sensor and dashboard example" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel k-right">
<div class="k-eyebrow">business mechanics</div>
<h1 class="k-title">Unit economics: hardware must pay for itself.</h1>
<p class="k-body">Pricing is not only “cost plus margin.” Hardware pricing must survive manufacturing, warranty, support, sales, and revisions.</p>

<div class="k-grid2">
<div class="k-card">
<strong>COGS</strong>
<span>Direct cost to build and deliver one unit.</span>
</div>

<div class="k-card">
<strong>BOM</strong>
<span>Parts and components inside that unit cost.</span>
</div>

<div class="k-card">
<strong>Hidden costs</strong>
<span>Returns, installation, warranty, support, and failed batches.</span>
</div>

<div class="k-card">
<strong>Recurring revenue</strong>
<span>Subscriptions, premium support, and service contracts.</span>
</div>

<div class="k-card k-wide k-accent">
<strong>Gross margin</strong>
<span>What remains after unit cost, before operating expenses.</span>
</div>
</div>

<p class="k-term">COGS = Cost of Goods Sold · BOM = Bill of Materials · Gross margin = selling price minus direct unit cost.</p>
</div>

<div class="k-media-panel k-left">
<img src="/unit-economics.png" alt="hardware unit economics flowchart" />
</div>
</div>

---
layout: default
class: text-white
---

<div class="k-slide">
<div class="k-text-panel">
<div class="k-eyebrow">what comes next</div>
<h1 class="k-title">After MVP, the job becomes validation to scale.</h1>
<p class="k-body">This is where engineering validation, design validation, production validation, certification, and mass production enter the picture.</p>

<div class="k-grid2">
<div class="k-card">
<strong>EVT</strong>
<span>Engineering Validation Test. Prove the core engineering works.</span>
</div>

<div class="k-card">
<strong>DVT</strong>
<span>Design Validation Test. Prove the design is stable and robust.</span>
</div>

<div class="k-card">
<strong>PVT</strong>
<span>Production Validation Test. Prove the factory can build it repeatedly.</span>
</div>

<div class="k-card">
<strong>Certification</strong>
<span>FCC, CE, EMC, and safety determine market access.</span>
</div>

<div class="k-card k-wide k-accent">
<strong>Mass production</strong>
<span>Focus on yield, quality assurance, suppliers, support, and repeatability.</span>
</div>
</div>

<p class="k-term">FCC = U.S. communications and emissions compliance · CE = European conformity marking · EMC = Electromagnetic Compatibility · QA = Quality Assurance.</p>
</div>

<div class="k-media-panel">
<img src="/after-mvp-roadmap.png" alt="after MVP roadmap" />
</div>
</div>

---
layout: center
class: text-white
---

<div style="position:absolute; inset:0; display:flex; align-items:center; justify-content:center; padding:2.5rem 4rem; overflow:hidden;">
<div style="position:relative; z-index:2; width:min(52rem, calc(100vw - 8rem)); text-align:center; padding:1.8rem 2.2rem; border-radius:1.75rem; border:1px solid rgba(255,255,255,.13); background:rgba(8,10,13,.76); box-shadow:0 24px 70px rgba(0,0,0,.32); backdrop-filter:blur(18px);">
<h1 style="margin:0; color:#f5f7fa; font-size:3.25rem; line-height:1.02; letter-spacing:-.05em; font-weight:820;">
The blink is the beginning.
</h1>

<p style="max-width:36rem; margin:.9rem auto 0; color:#b8c0cc; font-size:.95rem; line-height:1.45;">
The real product is everything after that: customer pain, deep engineering, validation, manufacturing, useful software, clear economics, and repeatable sales.
</p>

<div style="width:27rem; height:10.5rem; margin:1.35rem auto 0; border-radius:1.2rem; border:1px solid rgba(255,255,255,.11); overflow:hidden; background:rgba(255,255,255,.025);">
<img
  src="/cover-product-journey.png"
  alt="product development journey"
  style="width:100%; height:100%; object-fit:cover; object-position:center; display:block;"
/>
</div>
</div>
</div>

---
layout: default
class: text-white
---

<div style="position:absolute; inset:0; display:flex; align-items:center; justify-content:center; padding:3.2rem 4rem; overflow:hidden;">
<a href="https://www.youtube.com/watch?v=TYcfC-adRvA" target="_blank" rel="noopener noreferrer" style="position:relative; display:block; width:min(68rem, calc(100vw - 8rem)); height:min(34rem, calc(100vh - 7rem)); border-radius:1.8rem; border:1px solid rgba(255,255,255,.12); overflow:hidden; background:rgba(255,255,255,.03); box-shadow:0 28px 90px rgba(0,0,0,.34); text-decoration:none;">
<img src="https://img.youtube.com/vi/TYcfC-adRvA/maxresdefault.jpg" alt="Sample showcase video thumbnail" style="width:100%; height:100%; object-fit:cover; object-position:center; display:block;" />
<div style="position:absolute; inset:0; background:linear-gradient(180deg, rgba(0,0,0,.04) 0%, rgba(0,0,0,.12) 55%, rgba(0,0,0,.65) 100%);"></div>
<div style="position:absolute; left:50%; top:50%; transform:translate(-50%, -50%); width:5rem; height:5rem; display:flex; align-items:center; justify-content:center; border-radius:999px; border:1px solid rgba(255,255,255,.24); background:rgba(8,10,13,.78); box-shadow:0 18px 50px rgba(0,0,0,.42); backdrop-filter:blur(12px);">
<span style="margin-left:.22rem; color:#f5f7fa; font-size:2rem; line-height:1;">▶</span>
</div>
<div style="position:absolute; left:1.25rem; right:1.25rem; bottom:1.25rem; display:flex; align-items:center; justify-content:space-between; gap:1rem; padding:.95rem 1rem; border-radius:1.1rem; border:1px solid rgba(255,255,255,.1); background:rgba(8,10,13,.72); box-shadow:0 18px 50px rgba(0,0,0,.28); backdrop-filter:blur(14px);">
<div style="min-width:0;">
<div style="margin-top:.28rem; color:#f5f7fa; font-size:.8rem; line-height:1.2; font-weight:800;">Real sample process (yourTMJ Pen)</div>
<div style="margin-top:.22rem; color:#b8c0cc; font-size:.72rem; line-height:1.35; overflow:hidden; text-overflow:ellipsis; white-space:nowrap;">youtube.com/watch?v=TYcfC-adRvA</div>
</div>
<div style="display:inline-flex; align-items:center; gap:.5rem; flex-shrink:0; padding:.7rem .95rem; border-radius:.85rem; border:1px solid rgba(255,184,74,.26); background:rgba(255,184,74,.09); color:#ffbf5d; font-size:.72rem; font-weight:800;">
<span style="font-size:.95rem;">▶</span>
<span>Open</span>
</div>
</div>
</a>
</div>

---
layout: center
class: text-white
---

<div style="position:absolute; inset:0; display:flex; align-items:center; justify-content:center; padding:3rem 4rem; overflow:hidden;">
<div style="width:min(25rem); padding:2rem 2.2rem; border-radius:1.8rem; border:1px solid rgba(255,255,255,.12); background:rgba(8,10,13,.82); box-shadow:0 28px 90px rgba(0,0,0,.34); backdrop-filter:blur(18px);">
<div style="text-align:center; color:#62f5ee; text-transform:uppercase; letter-spacing:.22em; font-size:.68rem; font-weight:800;">Contact me</div>
<div style="display:grid; grid-template-columns:repeat(2, minmax(0, 1fr)); gap:.7rem; margin-top:1.35rem;">
<a href="mailto:fakhrip@protonmail.com" style="display:block; padding:.8rem .9rem; border-radius:.9rem; border:1px solid rgba(255,255,255,.1); background:rgba(16,19,23,.72); color:#f5f7fa; text-decoration:none;"><strong style="display:block; font-size:.72rem;">Email</strong><span style="display:block; margin-top:.2rem; color:#b8c0cc; font-size:.66rem;">fakhrip@protonmail.com</span></a>
<a href="https://fakhrip.github.io" target="_blank" rel="noopener noreferrer" style="display:block; padding:.8rem .9rem; border-radius:.9rem; border:1px solid rgba(255,255,255,.1); background:rgba(16,19,23,.72); color:#f5f7fa; text-decoration:none;"><strong style="display:block; font-size:.72rem;">Website</strong><span style="display:block; margin-top:.2rem; color:#b8c0cc; font-size:.66rem;">fakhrip.github.io</span></a>
<a href="https://www.instagram.com/fakhri_ptr/" target="_blank" rel="noopener noreferrer" style="display:block; padding:.8rem .9rem; border-radius:.9rem; border:1px solid rgba(255,255,255,.1); background:rgba(16,19,23,.72); color:#f5f7fa; text-decoration:none;"><strong style="display:block; font-size:.72rem;">Instagram</strong><span style="display:block; margin-top:.2rem; color:#b8c0cc; font-size:.66rem;">@fakhri_ptr</span></a>
<a href="https://youtube.com/@fakhri_ptr" target="_blank" rel="noopener noreferrer" style="display:block; padding:.8rem .9rem; border-radius:.9rem; border:1px solid rgba(255,255,255,.1); background:rgba(16,19,23,.72); color:#f5f7fa; text-decoration:none;"><strong style="display:block; font-size:.72rem;">YouTube</strong><span style="display:block; margin-top:.2rem; color:#b8c0cc; font-size:.66rem;">@fakhri_ptr</span></a>
<div style="grid-column:1 / -1; padding:.8rem .9rem; border-radius:.9rem; border:1px solid rgba(255,184,74,.24); background:rgba(255,184,74,.07);"><strong style="display:block; color:#ffbf5d; font-size:.72rem;">Discord</strong><span style="display:block; margin-top:.2rem; color:#c6cbd2; font-size:.66rem;">f4r4w4y</span></div>
</div>
</div>
</div>
