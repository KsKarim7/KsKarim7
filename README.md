<div align="center">

# Khaled Saifullah Karim

### AI Engineer · Deep Learning Researcher · Production Backend Developer

<p>
  <a href="https://linkedin.com/in/kskarim17"><img src="https://img.shields.io/badge/LinkedIn-kskarim17-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:kskarim177@gmail.com"><img src="https://img.shields.io/badge/Email-kskarim177%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://spiffy-elf-04f3d8.netlify.app"><img src="https://img.shields.io/badge/Portfolio-netlify.app-00C7B7?style=flat-square&logo=netlify&logoColor=white" alt="Portfolio"></a>
  <a href="https://twitter.com/KsKarim7"><img src="https://img.shields.io/badge/X-%40KsKarim7-000000?style=flat-square&logo=x&logoColor=white" alt="X / Twitter"></a>
</p>

<p>
  <img src="https://img.shields.io/badge/Based_in-Dhaka,_Bangladesh-555555?style=flat-square" alt="Dhaka, Bangladesh">
  <img src="https://img.shields.io/badge/B.Sc._CSE-BRAC_University-3B6EA5?style=flat-square" alt="BRAC University">
  <img src="https://img.shields.io/badge/Currently-AI_Engineering_Intern_%40_Thealon-6C3FB5?style=flat-square" alt="Current role">
</p>

</div>

I build **LLM applications with verification designed in** — outputs grounded in their source, checked in code, validated as structured output, with fallbacks and thorough tests — and I do **deep learning research in PyTorch** on parameter-efficient prompt learning for multimodal defect detection under missing sensors, and on medical image segmentation.

My working rule in research: **reproduce the baseline before extending it, and isolate every contribution with an ablation.** My working rule in engineering: **if the model says it, the code should be able to check it.** Two of the contract systems I built as sole developer run client businesses in Dhaka every day.

---

## 🔬 Research

### Reliability-Aware Multimodal Surface Defect Detection Under Uncertain Sensor Availability
**First author · Manuscript in preparation · 2025–26** &nbsp;·&nbsp; [📄 Paper](https://drive.google.com/file/d/1jS9I-kNvvtckyPhXLkasEg8ZzqAA6km3/view?usp=sharing) &nbsp;·&nbsp; [💻 Code](https://github.com/KsKarim7/Reliability-Aware-Multimodal-Surface-Defect-Detection-Under-Uncertain-Sensor-Availability)

- Extended the **MISDD-MM** missing-modality framework (cross-modal prompt learning over a frozen **CLIP** backbone) with four near-zero-initialised modules: intra-modal correlated prompting, input-conditioned dynamic prompts, multi-granularity text guidance, and continuous sensor-reliability weighting from RGB sharpness and depth density.
- **78.44% image-level AUROC** on MVTec 3D-AD under the dynamic both-missing protocol at a 70% missing rate, vs. a **73.83%** baseline (single seed), with a per-module ablation; **74.15%** on Eyecandies without retuning.
- Reproduced the baseline across four missing rates and three seeds *before* extending it.

### Enhanced U-Net for Spleen Segmentation in CT Scans
**Course research project · 2024** &nbsp;·&nbsp; [📄 Paper](https://drive.google.com/file/d/1esnroYYVgzOa3I180K4L0too5sPFkxJ5/view?usp=sharing)

- 2D U-Net that takes **three adjacent CT slices as input channels** for volumetric context, trained with a combined Dice + binary cross-entropy loss on the Medical Segmentation Decathlon spleen task.
- Studied the effect of slice context, loss weighting and data augmentation; applied **Grad-CAM** to diagnose failure modes such as spleen–kidney confusion, targeting clinical use in splenic volumetry and trauma assessment.

---

## 🚀 Featured Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/KsKarim7/Podcast-Compass">🎧 Podcast Compass</a></h3>
      <p><b>Grounded podcast study companion</b> · <a href="https://podcast-compass.streamlit.app">Live app</a></p>
      <p>Turns a transcript (.txt / .vtt / .srt / pasted) into a summary, navigable chapters and an interactive quiz. <b>Every claim is checkable:</b> each takeaway, chapter and quiz answer cites a transcript segment and an exact quote that server-side code verifies; unverifiable items are dropped or flagged, and timestamps come only from subtitle cues, never from the model.</p>
      <p>Pydantic-validated structured output · fallback model + repair retry · layered prompt-injection defences · thread-safe request counter · <b>312 pytest tests</b>.</p>
      <p><code>Python</code> <code>Streamlit</code> <code>Pydantic</code> <code>Gemini API</code> <code>pytest</code></p>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/KsKarim7/Genai-image-bench">🖼️ Genai Image Bench</a></h3>
      <p><b>Blind-scored text-to-image benchmark</b></p>
      <p>Harness comparing generative image providers on production criteria — prompt fidelity, in-image text rendering, character consistency, style adherence — with <b>human scoring blinded end to end</b> and provider identity rejoined only at report time.</p>
      <p>Records first-attempt vs. post-retry success, latency distribution and a failure taxonomy alongside quality, so reliability and output quality are reported separately. Across nine text-rendering prompts and three models from two vendors, none produced the requested string — reported as indistinguishable rather than force-ranked.</p>
      <p><code>Python</code> <code>asyncio</code> <code>httpx</code> <code>Cloudflare Workers AI</code> <code>pytest</code></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/KsKarim7/Reliability-Aware-Multimodal-Surface-Defect-Detection-Under-Uncertain-Sensor-Availability">🔍 Reliability-Aware Multimodal Defect Detection</a></h3>
      <p><b>Research code</b> · prompt learning over frozen CLIP for RGB + depth anomaly detection under missing modalities</p>
      <p>Baseline reproduction across four missing rates × three seeds, four extension modules, per-module ablations, and evaluation on MVTec 3D-AD and Eyecandies. See the Research section above for results.</p>
      <p><code>PyTorch</code> <code>CLIP</code> <code>Prompt learning</code> <code>Anomaly detection</code></p>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/KsKarim7/NewLife">🏪 HolyLife</a></h3>
      <p><b>Inventory &amp; operations system for a pharmacy</b> · <a href="https://holylife.store">Live</a> · in daily use by the client</p>
      <p>Stock with buying/selling price and on-hand vs. reserved quantities, customer orders with partial- and due-payment handling, supplier purchases and returns, expenses, VAT-compliant reports and thermal-printer receipts for in-store sales. Built end to end as sole developer, including handover docs.</p>
      <p><code>React</code> <code>TypeScript</code> <code>Node.js</code> <code>Express</code> <code>MongoDB</code> <code>JWT</code> <code>Cloudinary</code></p>
    </td>
  </tr>
</table>

---

## 💼 Experience

**AI Engineering Intern — Thealon Animation Studios** · Dhaka (Remote) · *Present*
Researching and prototyping with generative AI models, tools and APIs across image, video, audio and text, working directly with the founding team. Building API integrations and automation workflows that bring generative AI into the studio's internal tools and creative pipeline; testing and comparing tools for specific creative use cases and documenting findings for the team.

**Full-Stack Developer (Contract)** · Client projects, Remote · *2023 – 2025*
Delivered production systems for small businesses in Dhaka as sole developer — requirements, data modelling, deployment and handover. Two are in daily use: a clinic's visit and billing system (**HealthLink**) and a retail pharmacy's inventory and accounting system (**HolyLife**). Owned post-launch support end to end, including a repair script that resynced invoice numbering after duplicate-key collisions, and wrote setup guides and recovery procedures so clients can operate without me.

**B.Sc. in Computer Science and Engineering — BRAC University**, Dhaka · *Sep 2022 – Sep 2026*
Coursework: Machine Learning, Neural Networks, Computer Vision, Natural Language Processing, Data Science, Competitive Programming, Data Structures & Algorithms, Linear Algebra, Probability & Statistics.

---

## 🛠️ Technical Stack

**Languages**
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL">
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++">
</p>

**ML & Deep Learning**
<p>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white" alt="TensorFlow">
  <img src="https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white" alt="Keras">
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn">
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV">
  <img src="https://img.shields.io/badge/CLIP-412991?style=flat-square" alt="CLIP">
  <img src="https://img.shields.io/badge/U--Net-2E8B57?style=flat-square" alt="U-Net">
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy">
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas">
</p>

**Generative AI & LLM Engineering**
<p>
  <img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini API">
  <img src="https://img.shields.io/badge/Anthropic_API-191919?style=flat-square&logo=anthropic&logoColor=white" alt="Anthropic API">
  <img src="https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI API">
  <img src="https://img.shields.io/badge/Cloudflare_Workers_AI-F38020?style=flat-square&logo=cloudflare&logoColor=white" alt="Cloudflare Workers AI">
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white" alt="Pydantic">
</p>

Structured output with Pydantic · grounded-output verification · prompt-injection defences · prompt learning

**Backend, Data & Tooling**
<p>
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white" alt="Express">
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React">
  <img src="https://img.shields.io/badge/Django_REST-092E20?style=flat-square&logo=django&logoColor=white" alt="Django REST Framework">
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest">
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git">
</p>

---

## 📜 Certifications

- **Programming Hero — Complete Web Development, Batch 5 (2022)** · Black Belt graduate; certificate notes completion in the top 5% of the cohort
- **DataCamp — Reinforcement Learning (2026)** · Deep RL in Python · RL with Gymnasium · RL from Human Feedback (RLHF) · RL in Python
- **DataCamp — Machine Learning (2025–26)** · Introduction to Deep Learning in Python · Supervised Learning with scikit-learn · Feature Engineering for ML · Cleaning Data in Python

---

## 📊 GitHub Activity

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=KsKarim7&show_icons=true&theme=github_dark&hide_border=true&bg_color=00000000&include_all_commits=true&count_private=true">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=KsKarim7&show_icons=true&theme=default&hide_border=true&bg_color=00000000&include_all_commits=true&count_private=true" alt="GitHub stats">
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=KsKarim7&layout=compact&theme=github_dark&hide_border=true&bg_color=00000000&langs_count=8">
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=KsKarim7&layout=compact&theme=default&hide_border=true&bg_color=00000000&langs_count=8" alt="Top languages">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com?user=KsKarim7&theme=github-dark&hide_border=true&background=00000000">
  <img src="https://streak-stats.demolab.com?user=KsKarim7&theme=default&hide_border=true&background=00000000" alt="Contribution streak">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-activity-graph.vercel.app/graph?username=KsKarim7&theme=github-compact&hide_border=true&bg_color=00000000&area=true">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=KsKarim7&theme=minimal&hide_border=true&bg_color=00000000&area=true" alt="Contribution activity graph">
</picture>

</div>

---

<div align="center">

**Open to AI/ML engineering and research roles.** &nbsp;·&nbsp; [📄 Résumé](https://drive.google.com/file/d/1btM79sESSt89NsPrA_K4dbpW9QzlWCct/view?usp=sharing) &nbsp;·&nbsp; [💼 LinkedIn](https://linkedin.com/in/kskarim17) &nbsp;·&nbsp; [✉️ kskarim177@gmail.com](mailto:kskarim177@gmail.com)

<sub>Fun fact: I am not funny.</sub>

</div>
