---
title: Space AI Forum 2026
layout: default
---
{% assign ZENODO_URL = 'https://zenodo.org/communities/saf-proceedings/' %}

<link rel="icon" href="{{ '/favicon.ico' | relative_url }}">

<script>
document.addEventListener('DOMContentLoaded', function () {
  function setThemeColor(color) {
    let m = document.querySelector('meta[name="theme-color"]');
    if (!m) { m = document.createElement('meta'); m.name = 'theme-color'; document.head.appendChild(m); }
    m.setAttribute('content', color);
  }
  setThemeColor('#000000');
});
</script>

<script>
document.addEventListener('DOMContentLoaded', function(){
  const header = document.querySelector('.page-header');
  if (!header) return;

  // tagline comes from _config.yml but we override it here for the strategic update
  const tagline = header.querySelector('.project-tagline');
  if (tagline) {
    tagline.textContent = 'Advancing Autonomy and Intelligence in Orbit';
  }

  // 3rd line: make it share the tagline class so style matches exactly
  let dateLine = header.querySelector('.saf-date');
  if (!dateLine) {
    dateLine = document.createElement('p');
    dateLine.className = 'project-tagline saf-date';
    (tagline || header).insertAdjacentElement('afterend', dateLine);
  }
  // Merged line to clarify it is a workshop + date
  dateLine.textContent = 'Online workshop on AI for space • 14 Mar 2026';

  // button right under the date line
  let b = header.querySelector('.btn');
  if (!b) {
    b = document.createElement('a');
    b.className = 'btn';
    dateLine.insertAdjacentElement('afterend', b);
  }
  b.textContent = 'Call for Papers';
  b.href = 'https://openreview.net/group?id=SAF%2F2026%2FConference';
  b.target = '_blank';
  b.rel = 'noopener';
  b.style.setProperty('margin-top','0','important');
});
</script>

<style>
/* Hide the GitHub Pages footer */
.site-footer, .site-footer-credits, .site-footer-owner { display:none !important; }
</style>

<script>
document.addEventListener('DOMContentLoaded', function () {
  ['.site-footer', '.site-footer-owner', '.site-footer-credits']
    .forEach(sel => { const n = document.querySelector(sel); if (n) n.remove(); });
});
</script> 

<nav class="topnav" markdown="1">
[Overview](#overview) • [Why Space AI?](#why-space-ai) • [Dates](#important-dates) • [CFP](#call-for-papers) • [Submit](#submission) • [Committee](#committee) • [Program](#program) • [Contact](#contact)
</nav>

<style>
.topnav{position:sticky;top:0;z-index:9;background:#fff;text-align:center;padding:.5rem 0;border-bottom:1px solid #eaeaea}
.topnav p{margin:0}
.topnav a{margin:0 .35rem}
.main-content{padding-top:0}
@media (max-width:640px){.topnav a{display:inline-block;margin:.2rem .45rem}}
</style>

<!-- Option B image header -->
<style>
/* Image header with dark overlay for readability */
.page-header{
  background:
    linear-gradient(rgba(0,0,0,.55), rgba(0,0,0,.55)),
    url("{{ '/space_ai_forum_hero.jpg' | relative_url }}") center/cover no-repeat !important;
  color:#fff;
}
.page-header .project-name,
.page-header .project-tagline{color:#fff}
.page-header .btn{
  background:transparent;border:1px solid rgba(255,255,255,.9);color:#fff
}
.page-header .btn:hover{background:#fff;color:#000}
</style>

<style>
/* Make the two lines tighter and a bit smaller */
.page-header .project-tagline{
  color: rgba(255,255,255,.85);
  font-weight: 400;
  line-height: 1.35;
  font-size: clamp(16px, 2vw, 18px);
  margin: 12px 0 4px;               /* small gap: tagline → date */
}

/* The date line (it has class "project-tagline saf-date") */
.page-header .project-tagline.saf-date{
  margin-top: 0;
  margin-bottom: 25px;           /* space above the button */
}

/* Button sits right under the date line */
.page-header .btn{ margin-top:0 !important; }
</style>

<style>
/* Section heading color */
.main-content h2,
.main-content h3 { color:#3d85c6; } 
</style>

<style>
/* Big rounded logo to the left of the first Overview paragraph (lowered a bit) */
h2#overview + p{
  position: relative;
  padding-left: 96px;   /* space for the tile */
  min-height: 76px;
}
h2#overview + p::before{
  content:"";
  position:absolute; left:0;
  top:.34em;                 /* lowered to align with first-line caps */
  width:76px; height:76px;
  background:#fff url("{{ '/space_ai_forum_logo.jpg' | relative_url }}") center/80% no-repeat;
  border-radius:12px;
  box-shadow:0 2px 6px rgba(0,0,0,.2);
}

/* Align the second Overview paragraph with the first paragraph's text */
h2#overview + p + p{ padding-left:96px; }

@media (max-width:640px){
  h2#overview + p{ padding-left:82px; min-height:64px; }
  h2#overview + p::before{
    width:64px; height:64px;
    top:.28em;              /* slightly less offset on phones */
  }
  h2#overview + p + p{ padding-left:82px; }
}
</style>

## Overview
Space AI Forum gathers researchers and practitioners working on AI for satellites, planetary robotics, ground and flight segments, mission operations, and science data systems. The focus is practical exchange across algorithms, hardware, safety, and deployment.

Accepted work will be listed across official channels and, with author consent, disseminated through disciplinary mailing lists, institutional newsletters, and the organizers’ professional networks to strengthen readership and collaboration.

## Why Space AI? {#why-space-ai}
Artificial intelligence is the strategic accelerator for the new space economy. As space systems become Critical National Infrastructure, AI is essential for ensuring resilience, managing orbital congestion, and unlocking commercial growth. This forum moves beyond theory, providing the technical foundation required to turn these high-level ambitions into operational reality.

## Important dates

<style>
.saf-dates-wrapper {
  border: 1px solid #eaeaea;
  border-radius: 8px;
  overflow: hidden;
  margin-top: 16px;
  margin-bottom: 32px;
}
.saf-date-row {
  display: flex;
  border-bottom: 1px solid #eaeaea;
  background: #fff;
  transition: background 0.2s;
}
.saf-date-row:last-child {
  border-bottom: none;
}
.saf-date-row:hover {
  background: #fcfcfc;
}
.saf-date-left {
  width: 130px;
  padding: 14px 16px;
  background: #f6f8fa;
  border-right: 1px solid #eaeaea;
  font-weight: 600;
  color: #444;
  font-size: 15px;
  flex-shrink: 0;
  display: flex;
  align-items: center;
}
.saf-date-right {
  padding: 14px 16px;
  flex-grow: 1;
  color: #24292e;
  font-size: 16px;
  display: flex;
  align-items: center;
}
/* Highlight styles */
.saf-deadline .saf-date-left {
  color: #d73a49; /* Red for deadline */
  background: #fff5f5;
}
.saf-deadline .saf-date-right {
  font-weight: 600;
}
.saf-event-day .saf-date-left {
  color: #0366d6; /* Blue for event */
  background: #f1f8ff;
}
.saf-tz-note {
  font-size: 13px;
  color: #6a737d;
  margin-top: 8px;
  font-style: italic;
}

@media (max-width: 600px) {
  .saf-date-row { flex-direction: column; }
  .saf-date-left { width: 100%; border-right: none; border-bottom: 1px solid #eaeaea; padding: 10px 16px; }
  .saf-date-right { padding: 12px 16px; }
}
</style>

<div class="saf-dates-wrapper">
  <!-- Row 1 -->
  <div class="saf-date-row">
    <div class="saf-date-left">1 Nov 2025</div>
    <div class="saf-date-right">Submissions open</div>
  </div>
  <!-- Row 2: Deadline (Highlighted) -->
  <div class="saf-date-row saf-deadline">
    <div class="saf-date-left">29 Jan 2026</div>
    <div class="saf-date-right">Submission deadline (23:59 AoE)</div>
  </div>
  <!-- Row 3 -->
  <div class="saf-date-row">
    <div class="saf-date-left">17 Feb 2026</div>
    <div class="saf-date-right">Notifications</div>
  </div>
  <!-- Row 4 -->
  <div class="saf-date-row">
    <div class="saf-date-left">3 Mar 2026</div>
    <div class="saf-date-right">Camera-ready due</div>
  </div>
  <!-- Row 5: Event (Highlighted) -->
  <div class="saf-date-row saf-event-day">
    <div class="saf-date-left">14 Mar 2026</div>
    <div class="saf-date-right">Workshop Event (Online)</div>
  </div>
</div>

<p class="saf-tz-note">
  * AoE = Anywhere on Earth (UTC−12). This effectively means the deadline is valid as long as it is still the date mentioned anywhere on the planet.
</p>

## Call for Papers
We welcome short papers reporting research, negative results with lessons, systems notes, or position pieces.

<style>
.topics-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 12px;
  margin-top: 16px;
  margin-bottom: 32px;
}
.topic-item {
  background: #fff;
  border: 1px solid #eaeaea;
  border-radius: 6px;
  padding: 12px 16px;
  font-size: 15px;
  color: #444;
  display: flex;
  align-items: center;
  line-height: 1.4;
}
.topic-item:hover {
  border-color: #3d85c6;
  background: #fcfcfc;
}
</style>

<div class="topics-grid">
  <div class="topic-item">Autonomy for flight and surface assets</div>
  <div class="topic-item">On-board learning and inference</div>
  <div class="topic-item">Sensing, perception, tracking, and navigation</div>
  <div class="topic-item">Verification, validation, and testing</div>
  <div class="topic-item">Robustness to faults and radiation</div>
  <div class="topic-item">Scheduling and resource management</div>
  <div class="topic-item">Communications and federated methods</div>
  <div class="topic-item">LLMs and agents for ops and ground tools</div>
  <div class="topic-item">Data pipelines from lab to orbit</div>
  <div class="topic-item">Science applications in EO and planetary</div>
  <div class="topic-item">Mission science planning</div>
  <div class="topic-item">Ethics, safety, policy, and standards</div>
</div>

## Author kit

<style>
.author-kit-box {
  background: #f9f9f9;
  border: 1px solid #eaeaea;
  border-radius: 8px;
  padding: 24px;
  margin-bottom: 32px;
}
.author-kit-box ul {
  margin: 0;
  padding-left: 20px;
}
.author-kit-box li {
  margin-bottom: 8px;
  color: #333;
  line-height: 1.5;
}
</style>

<div class="author-kit-box">
  <ul>
    <li>Submissions should be 4–6 pages (excluding references) and formatted as a PDF.</li>
    <li>The review process is double-blind. Please ensure all author names and affiliations are removed from the manuscript.</li>
    <li>Accepted camera-ready files will be published under the CC BY 4.0 license.</li>
    <li>Figures, tables, and external links are encouraged.</li>
    <li>Supplementary material (optional) may be included as a separate PDF or ZIP file, provided it is also anonymized.</li>
    <li>Concurrent submissions are permitted only if the other venue allows it. Please disclose this in your submission.</li>
    <li>We encourage authors to share anonymized code or data via private links during review. After acceptance, you may release a public repository and add the link to OpenReview.</li>
  </ul>
</div>

## Submission

<style>
.submission-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 16px;
  margin-top: 16px;
  margin-bottom: 32px;
}
.submission-card {
  display: block;
  background: #fff;
  border: 1px solid #eaeaea;
  border-radius: 8px;
  padding: 20px;
  text-decoration: none !important;
  transition: all 0.2s ease;
}
.submission-card:hover {
  border-color: #3d85c6;
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.05);
}
.submission-card h4 {
  margin: 0 0 6px 0;
  color: #3d85c6;
  font-size: 16px;
  font-weight: 600;
}
.submission-card p {
  margin: 0;
  font-size: 14px;
  color: #586069;
  line-height: 1.4;
}
/* Highlight the main submit button */
.submission-card.primary {
  background: #f8faff;
  border-color: #cce1ff;
}
.submission-card.primary:hover {
  border-color: #3d85c6;
}
</style>

<div class="submission-grid">
  <a href="{{ '/saf2025_author_kit.zip' | relative_url }}" class="submission-card" target="_blank" rel="noopener">
    <h4>Download Template</h4>
    <p>Get the author kit (ZIP) or clone the Overleaf project.</p>
  </a>
  
  <a href="{{ '/Space_AI_Forum_2026_CFP.pdf' | relative_url }}" class="submission-card" target="_blank" rel="noopener">
    <h4>Download CFP</h4>
    <p>Get the 1-page Call for Papers as a PDF file.</p>
  </a>

  <a href="https://openreview.net/group?id=SAF%2F2026%2FConference" class="submission-card primary" target="_blank" rel="noopener">
    <h4>Start Submission</h4>
    <p>Upload your paper and supplementary material on OpenReview.</p>
  </a>
</div>

<p style="font-size:15px; color:#666; margin-top:-16px; margin-bottom:32px;">
  After acceptance, authors will be asked to upload a camera-ready version with names. We also encourage posting to arXiv.
</p>

## Committee

<style>
.committee-container {
  display: flex;
  flex-direction: column;
  gap: 24px;
  margin-top: 24px;
  margin-bottom: 32px;
}
.committee-card {
  display: flex;
  align-items: center;
  gap: 20px;
}
.committee-avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  object-fit: cover;
  border: 1px solid #eaeaea;
  flex-shrink: 0;
}
.committee-info h4 {
  margin: 0 0 2px 0;
  font-size: 17px;
  font-weight: 600;
  color: #24292e;
}
.committee-info p {
  margin: 0;
  font-size: 15px;
  color: #586069;
  line-height: 1.4;
}
.committee-general {
  font-style: italic;
  color: #586069;
  margin-top: 8px;
}
</style>

<div class="committee-container">
  <!-- Chair -->
  <div class="committee-card">
    <img class="committee-avatar" src="{{ '/images/sylvester-kaczmarek.jpeg' | relative_url }}" alt="Sylvester Kaczmarek">
    <div class="committee-info">
      <h4>Sylvester Kaczmarek</h4>
      <p>Program Chair</p>
    </div>
  </div>
  
  <!-- General Members -->
  <div class="committee-general">
    Program committee invited from academia and industry
  </div>
</div>

## Program
Highly selective single-track program (approx. 6 accepted papers)  
Invited talks 1–2 speakers, 20–30 minutes plus Q&A  
Format single track, live video with recordings published afterward  
Detailed schedule will appear here after notifications

## Presentation
Each accepted paper gets a 10-minute talk and a 5-minute Q&A  
Slides or short video due one week before the event  
Recordings published for authors who opt in

## Tentative schedule (GMT)

<style>
.saf-schedule-table {
  width: 100%;
  border-collapse: collapse;
  margin: 16px 0 32px 0;
  font-size: 16px;
}
.saf-schedule-table th, 
.saf-schedule-table td {
  padding: 12px 16px;
  border-bottom: 1px solid #eaeaea;
  text-align: left;
  vertical-align: top;
}
.saf-time-col {
  width: 140px;
  font-weight: 600;
  color: #555;
  white-space: nowrap;
}
.saf-event-col {
  color: #24292e;
}
@media (max-width: 600px) {
  .saf-time-col { width: 110px; font-size: 15px; }
}
</style>

<table class="saf-schedule-table">
  <tbody>
    <tr>
      <td class="saf-time-col">15:00–15:10</td>
      <td class="saf-event-col">Opening</td>
    </tr>
    <tr>
      <td class="saf-time-col">15:10–16:00</td>
      <td class="saf-event-col">Paper session 1</td>
    </tr>
    <tr>
      <td class="saf-time-col">16:00–16:20</td>
      <td class="saf-event-col">Invited talk</td>
    </tr>
    <tr>
      <td class="saf-time-col">16:20–16:30</td>
      <td class="saf-event-col">Break</td>
    </tr>
    <tr>
      <td class="saf-time-col">16:30–17:20</td>
      <td class="saf-event-col">Paper session 2</td>
    </tr>
    <tr>
      <td class="saf-time-col">17:20–17:45</td>
      <td class="saf-event-col">Panel and Q&A</td>
    </tr>
    <tr>
      <td class="saf-time-col">17:45–18:00</td>
      <td class="saf-event-col">Closing</td>
    </tr>
  </tbody>
</table>

## Registration and acknowledgments
Attendance is free for the first edition.
Thanks to the community for supporting this initiative.

## Proceedings
Accepted PDFs stay on OpenReview  
Archival copies with DOIs are deposited in the <a href="{{ ZENODO_URL }}" target="_blank" rel="noopener">Space AI Forum Zenodo Community</a>  
If you have an arXiv preprint, we’ll link it for you

## Call for reviewers
We welcome reviewers with expertise in space systems, robotics, autonomy, ML, and safety  
How to apply: email research@sylvesterkaczmarek.com with your homepage or Google Scholar and 3–5 keywords  
Service window Feb–Mar 2026. Expected load 2–3 papers

## Accessibility
Live captions will be enabled. If you need assistance, email research@sylvesterkaczmarek.com

## Policies
Be respectful and constructive. Harassment or discrimination is not tolerated  
Privacy notice: We collect only what is needed to run the event. Contact us for removal requests  
Recording consent: Speakers and authors will be asked to opt in before recording  
Conflicts: Authors may serve as reviewers with strict COI. No reviewing of one’s own paper, same institution, advisor or advisee, coauthors in the last 3 years, close collaborators, or active funding ties in the last 2 years  
Review model: Each paper receives at least two reviews and one meta review by the chair. The chair assigns reviews in OpenReview and enforces COI  
Review visibility: Double-blind during review. Reviews are posted on OpenReview. After decisions, accepted papers appear with author names  
Archiving consent: By submitting the camera-ready, you permit the organizers to archive it on Zenodo under CC BY 4.0 and mint a DOI  
Export control and dual-use: Do not submit ITAR/EAR-restricted, classified, or proprietary-restricted content. Authors must have the right to share any data or code included  
Code of conduct reports: Email research@sylvesterkaczmarek.com with subject “Conduct”

## Contact
Email research@sylvesterkaczmarek.com

<footer class="saf-footer">
  <img class="saf-logo" src="{{ '/space_ai_forum_logo.jpg' | relative_url }}" alt="Space AI Forum logo">
</footer>
<style>
.saf-footer{ text-align:center; margin:32px 0 36px; }
.saf-logo{
  display:block;
  margin:0 auto;
  height:72px;               /* keep your sizing */
  max-width:90vw;
  vertical-align:middle;
  background:#fff;           /* white tile */
  border-radius:12px;        /* rounded corners */
  padding:8px;               /* small inset to match the tile look */
  box-shadow:0 2px 6px rgba(0,0,0,.2);
}
@media (min-width:900px){ .saf-logo{ height:88px; } }
</style>

<hr class="saf-hr">
<p class="saf-copy">Copyright © Space AI Forum {{ 'now' | date: '%Y' }} • SpaceAI.org.uk</p>

<style>
.saf-hr{border:0;border-top:1px solid #eaeaea;margin:24px 0 8px}
.saf-copy{margin:0;text-align:center;color:#6b7280;font-size:14px}
</style>
