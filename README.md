
<style>
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;700&family=DM+Sans:wght@300;400;500;600&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
:root{--bg:#0d1117;--surface:#161b22;--surface2:#21262d;--border:#30363d;--text:#e6edf3;--muted:#7d8590;--accent:#7c3aed;--accent2:#06b6d4;--green:#3fb950;--mono:'JetBrains Mono',monospace;--sans:'DM Sans',sans-serif}
body{background:var(--bg);color:var(--text);font-family:var(--sans);padding:0;min-height:100vh}
.readme{max-width:680px;margin:0 auto;padding:1.5rem 1rem}
.header{text-align:center;padding:2rem 0 1.5rem;border-bottom:1px solid var(--border);margin-bottom:1.5rem}
.name-line{font-size:2rem;font-weight:600;font-family:var(--sans);letter-spacing:-0.5px;margin-bottom:0.25rem}
.name-line span{color:var(--accent)}
.tagline{font-size:0.85rem;color:var(--muted);font-family:var(--mono);margin-bottom:1rem;letter-spacing:0.5px}
.badges{display:flex;gap:6px;justify-content:center;flex-wrap:wrap;margin-bottom:0.75rem}
.badge{font-size:11px;font-family:var(--mono);padding:3px 10px;border-radius:20px;border:1px solid;font-weight:600;letter-spacing:0.3px}
.badge-purple{border-color:var(--accent);color:var(--accent);background:rgba(124,58,237,0.1)}
.badge-cyan{border-color:var(--accent2);color:var(--accent2);background:rgba(6,182,212,0.1)}
.badge-green{border-color:var(--green);color:var(--green);background:rgba(63,185,80,0.1)}
.section{margin-bottom:1.5rem}
.section-label{font-size:11px;font-family:var(--mono);color:var(--muted);text-transform:uppercase;letter-spacing:1.5px;margin-bottom:0.75rem;display:flex;align-items:center;gap:8px}
.section-label::after{content:'';flex:1;height:1px;background:var(--border)}
.yaml-block{background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:1rem 1.25rem;font-family:var(--mono);font-size:12px;line-height:1.8}
.yaml-key{color:var(--accent2)}
.yaml-val{color:var(--text)}
.yaml-str{color:#a5d6ff}
.yaml-tag{color:var(--green)}
.yaml-comment{color:var(--muted);font-style:italic}
.currently-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.curr-card{background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:0.875rem 1rem}
.curr-icon{font-size:16px;margin-bottom:6px}
.curr-title{font-size:12px;font-weight:600;color:var(--text);margin-bottom:2px}
.curr-desc{font-size:11px;color:var(--muted);line-height:1.5}
.curr-tag{font-size:10px;font-family:var(--mono);color:var(--accent);margin-top:6px}
.stack-group{margin-bottom:1rem}
.stack-group-name{font-size:11px;color:var(--muted);font-family:var(--mono);margin-bottom:6px}
.pills{display:flex;flex-wrap:wrap;gap:5px}
.pill{font-size:11px;font-family:var(--mono);padding:3px 9px;border-radius:4px;background:var(--surface2);border:1px solid var(--border);color:var(--text);font-weight:500}
.pill.hot{border-color:rgba(124,58,237,0.4);color:#c4b5fd}
.projects-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.proj-card{background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:0.875rem 1rem}
.proj-card.featured{border-color:rgba(124,58,237,0.5);background:rgba(124,58,237,0.05)}
.proj-top{display:flex;align-items:center;gap:6px;margin-bottom:4px}
.proj-icon{font-size:14px}
.proj-name{font-size:13px;font-weight:600;color:var(--text)}
.proj-desc{font-size:11px;color:var(--muted);line-height:1.5;margin-bottom:6px}
.proj-tech{display:flex;flex-wrap:wrap;gap:4px}
.proj-chip{font-size:10px;font-family:var(--mono);padding:1px 6px;border-radius:3px;background:var(--surface2);border:1px solid var(--border);color:var(--muted)}
.stats-row{display:grid;grid-template-columns:repeat(4,1fr);gap:8px}
.stat-card{background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:0.75rem;text-align:center}
.stat-num{font-size:20px;font-weight:600;font-family:var(--mono);color:var(--accent)}
.stat-label{font-size:10px;color:var(--muted);margin-top:2px;line-height:1.3}
.exp-list{display:flex;flex-direction:column;gap:8px}
.exp-item{display:flex;align-items:flex-start;gap:10px;background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:0.75rem 1rem}
.exp-dot{width:8px;height:8px;border-radius:50%;background:var(--green);margin-top:5px;flex-shrink:0}
.exp-title{font-size:13px;font-weight:500;color:var(--text)}
.exp-sub{font-size:11px;color:var(--muted);margin-top:2px}
.connect-row{display:flex;gap:8px;flex-wrap:wrap}
.connect-btn{display:flex;align-items:center;gap:6px;font-size:12px;font-family:var(--mono);padding:6px 12px;border-radius:6px;border:1px solid var(--border);color:var(--text);background:var(--surface);text-decoration:none;cursor:pointer;transition:border-color 0.15s}
.connect-btn:hover{border-color:var(--accent);color:var(--accent)}
.connect-btn .dot{width:7px;height:7px;border-radius:50%;background:var(--green);flex-shrink:0}
.footer{text-align:center;padding-top:1.5rem;border-top:1px solid var(--border);margin-top:1rem}
.footer p{font-size:12px;color:var(--muted);font-family:var(--mono);line-height:1.8}
.footer .quote{font-style:italic;color:var(--text);margin-bottom:4px}
.open-badge{display:inline-flex;align-items:center;gap:5px;font-size:11px;font-family:var(--mono);padding:3px 10px;border-radius:20px;border:1px solid var(--green);color:var(--green);background:rgba(63,185,80,0.08);margin-top:8px}
</style>

<div class="readme">

<div class="header">
  <div class="name-line">Hi, I'm <span>Dhanush G</span> 👋</div>
  <div class="tagline">// AI Engineer · Full Stack · Cybersecurity · Cloud</div>
  <div class="badges">
    <span class="badge badge-purple">B.Tech CSE · 2nd Year</span>
    <span class="badge badge-purple">Alliance University, Bangalore</span>
    <span class="badge badge-cyan">Open to Internships</span>
    <span class="badge badge-cyan">Open to Collaboration</span>
    <span class="badge badge-green">GSoC Aspirant</span>
  </div>
</div>

<div class="section">
  <div class="section-label">about</div>
  <div class="yaml-block">
    <div><span class="yaml-key">name        </span><span class="yaml-val">: </span><span class="yaml-str">Dhanush G</span></div>
    <div><span class="yaml-key">focus       </span><span class="yaml-val">: </span><span class="yaml-str">AI/ML · Full Stack · Cloud Security</span></div>
    <div><span class="yaml-key">university  </span><span class="yaml-val">: </span><span class="yaml-str">Alliance University, Bangalore</span> <span class="yaml-comment"># 2nd Year B.Tech CSE</span></div>
    <div><span class="yaml-key">status      </span><span class="yaml-val">: </span><span class="yaml-tag">Open to internships &amp; open-source 🟢</span></div>
    <div><span class="yaml-key">building    </span><span class="yaml-val">: </span><span class="yaml-str">AI Security Platform · ATS Resume AI · Cloud Resume</span></div>
    <div><span class="yaml-key">learning    </span><span class="yaml-val">: </span><span class="yaml-str">LLM fine-tuning · MLOps · Kubernetes · Rust</span></div>
    <div><span class="yaml-key">goal        </span><span class="yaml-val">: </span><span class="yaml-str">GSoC 2026 · Scalable intelligent systems</span></div>
    <div><span class="yaml-key">email       </span><span class="yaml-val">: </span><span class="yaml-str">dhanushgedu@gmail.com</span></div>
  </div>
</div>

<div class="section">
  <div class="section-label">currently working on</div>
  <div class="currently-grid">
    <div class="curr-card">
      <div class="curr-icon">🔒</div>
      <div class="curr-title">AI Security Monitoring Platform</div>
      <div class="curr-desc">Real-time threat detection using Isolation Forest ML, FastAPI backend, Next.js 3D globe dashboard</div>
      <div class="curr-tag">► 80+ commits · Dockerized · CI/CD</div>
    </div>
    <div class="curr-card">
      <div class="curr-icon">☁️</div>
      <div class="curr-title">Cloud Resume Website</div>
      <div class="curr-desc">Serverless AWS stack — S3, CloudFront, Lambda, DynamoDB, automated deploys via GitHub Actions</div>
      <div class="curr-tag">► Live HTTPS · Visitor counter</div>
    </div>
    <div class="curr-card">
      <div class="curr-icon">🤖</div>
      <div class="curr-title">LLM Fine-tuning & Agentic AI</div>
      <div class="curr-desc">Exploring LangChain agents, RAG pipelines, and cloud-native security architectures</div>
      <div class="curr-tag">► Research · Prototyping</div>
    </div>
    <div class="curr-card">
      <div class="curr-icon">🎯</div>
      <div class="curr-title">GSoC 2026 Prep</div>
      <div class="curr-desc">Contributing to open-source security tools, building GSOC-level projects and community presence</div>
      <div class="curr-tag">► Targeting security orgs</div>
    </div>
  </div>
</div>

<div class="section">
  <div class="section-label">tech stack</div>
  <div class="stack-group">
    <div class="stack-group-name">Languages</div>
    <div class="pills">
      <span class="pill hot">Python</span><span class="pill hot">TypeScript</span><span class="pill">JavaScript</span><span class="pill">C++</span><span class="pill">Java</span><span class="pill">Go</span><span class="pill">Rust</span><span class="pill">SQL</span>
    </div>
  </div>
  <div class="stack-group">
    <div class="stack-group-name">AI / ML</div>
    <div class="pills">
      <span class="pill hot">PyTorch</span><span class="pill hot">TensorFlow</span><span class="pill hot">LangChain</span><span class="pill">scikit-learn</span><span class="pill">Pandas</span><span class="pill">NumPy</span><span class="pill">Isolation Forest</span>
    </div>
  </div>
  <div class="stack-group">
    <div class="stack-group-name">Frontend / Backend</div>
    <div class="pills">
      <span class="pill hot">Next.js</span><span class="pill hot">FastAPI</span><span class="pill">React</span><span class="pill">Node.js</span><span class="pill">Django</span><span class="pill">TailwindCSS</span><span class="pill">Three.js</span>
    </div>
  </div>
  <div class="stack-group">
    <div class="stack-group-name">Cloud / DevOps</div>
    <div class="pills">
      <span class="pill hot">AWS</span><span class="pill">GCP</span><span class="pill hot">Docker</span><span class="pill">Kubernetes</span><span class="pill">GitHub Actions</span><span class="pill">Terraform</span>
    </div>
  </div>
  <div class="stack-group">
    <div class="stack-group-name">Security</div>
    <div class="pills">
      <span class="pill">Kali Linux</span><span class="pill">Wireshark</span><span class="pill">Metasploit</span><span class="pill">Splunk</span><span class="pill">AES Encryption</span><span class="pill">SIEM</span>
    </div>
  </div>
</div>

<div class="section">
  <div class="section-label">featured projects</div>
  <div class="projects-grid">
    <div class="proj-card featured">
      <div class="proj-top"><span class="proj-icon">🔒</span><span class="proj-name">AI Security Monitor</span></div>
      <div class="proj-desc">ML-powered threat detection. Isolation Forest anomaly engine, FastAPI backend, real-time 3D globe dashboard in Next.js.</div>
      <div class="proj-tech"><span class="proj-chip">Python</span><span class="proj-chip">FastAPI</span><span class="proj-chip">Next.js</span><span class="proj-chip">Three.js</span><span class="proj-chip">Docker</span></div>
    </div>
    <div class="proj-card featured">
      <div class="proj-top"><span class="proj-icon">🤖</span><span class="proj-name">ATS Score Booster</span></div>
      <div class="proj-desc">AI resume analyzer — scores against JDs, keyword gap analysis, formatting feedback, score dashboard.</div>
      <div class="proj-tech"><span class="proj-chip">Python</span><span class="proj-chip">NLP</span><span class="proj-chip">FastAPI</span><span class="proj-chip">React</span></div>
    </div>
    <div class="proj-card">
      <div class="proj-top"><span class="proj-icon">☁️</span><span class="proj-name">Cloud Resume</span></div>
      <div class="proj-desc">Serverless resume on AWS — S3, CloudFront, Lambda, DynamoDB, GitHub Actions CI/CD pipeline.</div>
      <div class="proj-tech"><span class="proj-chip">AWS</span><span class="proj-chip">Lambda</span><span class="proj-chip">DynamoDB</span><span class="proj-chip">GH Actions</span></div>
    </div>
    <div class="proj-card">
      <div class="proj-top"><span class="proj-icon">🛡️</span><span class="proj-name">Secure File Sharing</span></div>
      <div class="proj-desc">AES end-to-end encrypted file upload/download app. Built during Cybersecurity internship.</div>
      <div class="proj-tech"><span class="proj-chip">Python</span><span class="proj-chip">AES</span><span class="proj-chip">JavaScript</span></div>
    </div>
  </div>
</div>

<div class="section">
  <div class="section-label">stats</div>
  <div class="stats-row">
    <div class="stat-card"><div class="stat-num">208+</div><div class="stat-label">GitHub contributions last year</div></div>
    <div class="stat-card"><div class="stat-num">12+</div><div class="stat-label">public repositories</div></div>
    <div class="stat-card"><div class="stat-num">2nd</div><div class="stat-label">year B.Tech CSE</div></div>
    <div class="stat-card"><div class="stat-num">4+</div><div class="stat-label">domains: AI · web · cloud · sec</div></div>
  </div>
</div>

<div class="section">
  <div class="section-label">experience & credentials</div>
  <div class="exp-list">
    <div class="exp-item"><div class="exp-dot"></div><div><div class="exp-title">Cybersecurity Internship — Future Interns</div><div class="exp-sub">Network analysis · Splunk SIEM · Secure File Sharing system (Task 3)</div></div></div>
    <div class="exp-item"><div class="exp-dot"></div><div><div class="exp-title">Google Cloud Skills Boost</div><div class="exp-sub">Hands-on GCP labs · BigQuery · Kubernetes · Cloud networking</div></div></div>
    <div class="exp-item"><div class="exp-dot"></div><div><div class="exp-title">GSoC 2026 Aspirant</div><div class="exp-sub">Building open-source AI/security tools at GSoC contribution level</div></div></div>
  </div>
</div>

<div class="section">
  <div class="section-label">connect</div>
  <div class="connect-row">
    <a class="connect-btn" href="https://linkedin.com/in/dhanush-g-"><i class="ti ti-brand-linkedin" aria-hidden="true"></i>LinkedIn</a>
    <a class="connect-btn" href="https://dhanushgcode.github.io"><i class="ti ti-world" aria-hidden="true"></i>Portfolio</a>
    <a class="connect-btn" href="mailto:dhanushgedu@gmail.com"><i class="ti ti-mail" aria-hidden="true"></i>Email</a>
    <a class="connect-btn" href="https://github.com/DHANUSHGCODE"><i class="ti ti-brand-github" aria-hidden="true"></i>GitHub</a>
  </div>
</div>

<div class="footer">
  <p class="quote">"First, solve the problem. Then, write the code." — John Johnson</p>
  <p>⭐ If my work helps you, a star means a lot!</p>
  <div style="display:flex;justify-content:center;gap:8px;flex-wrap:wrap;margin-top:10px">
    <span class="open-badge"><span class="dot"></span>Open to internships</span>
    <span class="open-badge"><span class="dot"></span>Open to collaboration</span>
    <span class="open-badge"><span class="dot"></span>Open source contributor</span>
  </div>
</div>

</div>
