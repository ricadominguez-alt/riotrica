# ricadominguez
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rica Mae Dominguez — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --coral: #FF6B6B;
    --teal: #2EC4B6;
    --gold: #FFB347;
    --plum: #6B2D8B;
    --cream: #FFF8F0;
    --dark: #1A1A2E;
    --mid: #3D3D5C;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--dark);
    overflow-x: hidden;
  }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    background: var(--dark);
    display: grid;
    grid-template-columns: 1fr 1fr;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    width: 600px; height: 600px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(46,196,182,0.25) 0%, transparent 70%);
    top: -100px; right: -100px;
    pointer-events: none;
  }

  .hero::after {
    content: '';
    position: absolute;
    width: 400px; height: 400px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(255,107,107,0.2) 0%, transparent 70%);
    bottom: -80px; left: 100px;
    pointer-events: none;
  }

  .hero-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 80px 60px;
    position: relative;
    z-index: 2;
  }

  .hero-tag {
    display: inline-block;
    background: var(--teal);
    color: white;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 3px;
    text-transform: uppercase;
    padding: 6px 16px;
    border-radius: 20px;
    margin-bottom: 28px;
    width: fit-content;
    animation: fadeUp 0.6s ease both;
  }

  .hero-name {
    font-family: 'Playfair Display', serif;
    font-size: clamp(42px, 5vw, 68px);
    font-weight: 900;
    color: white;
    line-height: 1.05;
    margin-bottom: 20px;
    animation: fadeUp 0.6s 0.1s ease both;
  }

  .hero-name span { color: var(--coral); }

  .hero-subtitle {
    font-size: 16px;
    color: rgba(255,255,255,0.6);
    line-height: 1.7;
    max-width: 400px;
    margin-bottom: 40px;
    animation: fadeUp 0.6s 0.2s ease both;
  }

  .hero-roles {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    animation: fadeUp 0.6s 0.3s ease both;
  }

  .role-pill {
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.15);
    color: rgba(255,255,255,0.85);
    font-size: 13px;
    padding: 8px 18px;
    border-radius: 30px;
    backdrop-filter: blur(4px);
    transition: all 0.3s;
  }

  .role-pill:hover {
    background: var(--coral);
    border-color: var(--coral);
    color: white;
    transform: translateY(-2px);
  }

  .hero-right {
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
    z-index: 2;
    padding: 80px 60px;
  }

  .hero-visual {
    position: relative;
    width: 360px;
    height: 420px;
  }

  .avatar-card {
    width: 280px;
    height: 340px;
    background: linear-gradient(135deg, var(--plum), var(--teal));
    border-radius: 24px;
    position: absolute;
    top: 0; left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    box-shadow: 0 30px 60px rgba(0,0,0,0.4);
    animation: fadeUp 0.6s 0.2s ease both;
  }

  .avatar-initials {
    font-family: 'Playfair Display', serif;
    font-size: 72px;
    font-weight: 900;
    color: white;
    opacity: 0.9;
    letter-spacing: -2px;
    line-height: 1;
    margin-bottom: 12px;
  }

  .avatar-label {
    font-size: 12px;
    color: rgba(255,255,255,0.7);
    letter-spacing: 2px;
    text-transform: uppercase;
  }

  .float-badge {
    position: absolute;
    background: white;
    border-radius: 16px;
    padding: 12px 18px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    animation: float 3s ease-in-out infinite;
  }

  .float-badge.b1 {
    bottom: 30px; right: 0;
    animation-delay: 0s;
  }
  .float-badge.b2 {
    top: 40px; right: 10px;
    animation-delay: 1s;
  }
  .float-badge.b3 {
    top: 120px; left: 0;
    animation-delay: 2s;
  }

  .badge-emoji { font-size: 20px; display: block; text-align: center; }
  .badge-text { font-size: 10px; font-weight: 600; color: var(--dark); letter-spacing: 0.5px; text-align: center; margin-top: 2px; }

  /* ── SECTIONS ── */
  section { padding: 100px 0; }

  .container { max-width: 1100px; margin: 0 auto; padding: 0 40px; }

  .section-label {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 16px;
  }

  .section-label span:first-child {
    width: 36px; height: 3px;
    background: var(--coral);
    display: block;
    border-radius: 2px;
  }

  .section-label span:last-child {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--coral);
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(32px, 4vw, 48px);
    font-weight: 700;
    color: var(--dark);
    line-height: 1.15;
    margin-bottom: 56px;
  }

  /* ── ABOUT ── */
  .about { background: white; }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }

  .about-text p {
    font-size: 16px;
    line-height: 1.85;
    color: var(--mid);
    margin-bottom: 20px;
  }

  .about-text strong { color: var(--dark); font-weight: 600; }

  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }

  .stat-card {
    background: var(--cream);
    border-radius: 20px;
    padding: 28px 24px;
    position: relative;
    overflow: hidden;
    transition: transform 0.3s;
  }

  .stat-card:hover { transform: translateY(-4px); }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
  }

  .stat-card:nth-child(1)::before { background: var(--coral); }
  .stat-card:nth-child(2)::before { background: var(--teal); }
  .stat-card:nth-child(3)::before { background: var(--gold); }
  .stat-card:nth-child(4)::before { background: var(--plum); }

  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 42px;
    font-weight: 900;
    line-height: 1;
    margin-bottom: 6px;
  }

  .stat-card:nth-child(1) .stat-num { color: var(--coral); }
  .stat-card:nth-child(2) .stat-num { color: var(--teal); }
  .stat-card:nth-child(3) .stat-num { color: var(--gold); }
  .stat-card:nth-child(4) .stat-num { color: var(--plum); }

  .stat-label { font-size: 13px; color: var(--mid); font-weight: 500; }

  /* ── EXPERIENCE ── */
  .experience { background: var(--cream); }

  .exp-timeline {
    display: flex;
    flex-direction: column;
    gap: 32px;
  }

  .exp-card {
    background: white;
    border-radius: 24px;
    padding: 36px 40px;
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 32px;
    align-items: start;
    box-shadow: 0 4px 20px rgba(0,0,0,0.05);
    transition: transform 0.3s, box-shadow 0.3s;
    position: relative;
    overflow: hidden;
  }

  .exp-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 40px rgba(0,0,0,0.1);
  }

  .exp-card::after {
    content: '';
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 5px;
  }

  .exp-card:nth-child(1)::after { background: var(--coral); }
  .exp-card:nth-child(2)::after { background: var(--teal); }
  .exp-card:nth-child(3)::after { background: var(--gold); }
  .exp-card.exp-card-4::after  { background: var(--plum); }
  .exp-card.exp-card-5::after  { background: #4A90D9; }
  .exp-card.exp-card-6::after  { background: #E85D9A; }

  .exp-icon {
    width: 58px; height: 58px;
    border-radius: 16px;
    display: flex; align-items: center; justify-content: center;
    font-size: 26px;
    flex-shrink: 0;
  }

  .exp-card:nth-child(1) .exp-icon { background: rgba(255,107,107,0.12); }
  .exp-card:nth-child(2) .exp-icon { background: rgba(46,196,182,0.12); }
  .exp-card:nth-child(3) .exp-icon { background: rgba(255,179,71,0.12); }

  .exp-period {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-bottom: 6px;
  }
  .exp-card:nth-child(1) .exp-period { color: var(--coral); }
  .exp-card:nth-child(2) .exp-period { color: var(--teal); }
  .exp-card:nth-child(3) .exp-period { color: var(--gold); }
  .exp-card.exp-card-4 .exp-period   { color: var(--plum); }
  .exp-card.exp-card-5 .exp-period   { color: #4A90D9; }
  .exp-card.exp-card-6 .exp-period   { color: #E85D9A; }

  .exp-title {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    font-weight: 700;
    margin-bottom: 4px;
  }

  .exp-company {
    font-size: 14px;
    color: var(--mid);
    margin-bottom: 16px;
    font-weight: 500;
  }

  .exp-desc {
    font-size: 14px;
    line-height: 1.75;
    color: #666;
  }

  .exp-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 16px;
  }

  .exp-tag {
    font-size: 11px;
    font-weight: 600;
    padding: 4px 12px;
    border-radius: 20px;
    letter-spacing: 0.5px;
  }

  .exp-card:nth-child(1) .exp-tag { background: rgba(255,107,107,0.1); color: var(--coral); }
  .exp-card:nth-child(2) .exp-tag { background: rgba(46,196,182,0.1); color: var(--teal); }
  .exp-card:nth-child(3) .exp-tag { background: rgba(255,179,71,0.15); color: #b87c00; }
  .exp-card.exp-card-4 .exp-tag   { background: rgba(107,45,139,0.1); color: var(--plum); }
  .exp-card.exp-card-5 .exp-tag   { background: rgba(74,144,217,0.1); color: #4A90D9; }
  .exp-card.exp-card-6 .exp-tag   { background: rgba(232,93,154,0.1); color: #E85D9A; }

  /* ── SKILLS ── */
  .skills { background: var(--dark); }
  .skills .section-title { color: white; }
  .skills .section-label span:last-child { color: var(--teal); }
  .skills .section-label span:first-child { background: var(--teal); }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
  }

  .skill-group {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.08);
    border-radius: 24px;
    padding: 32px 28px;
    transition: background 0.3s;
  }

  .skill-group:hover { background: rgba(255,255,255,0.08); }

  .skill-group-icon { font-size: 32px; margin-bottom: 16px; }

  .skill-group-title {
    font-family: 'Playfair Display', serif;
    font-size: 18px;
    font-weight: 700;
    color: white;
    margin-bottom: 20px;
  }

  .skill-item {
    margin-bottom: 16px;
  }

  .skill-row {
    display: flex;
    justify-content: space-between;
    margin-bottom: 6px;
  }

  .skill-name { font-size: 13px; color: rgba(255,255,255,0.75); font-weight: 500; }
  .skill-pct { font-size: 12px; font-weight: 700; }

  .skill-group:nth-child(1) .skill-pct { color: var(--coral); }
  .skill-group:nth-child(2) .skill-pct { color: var(--teal); }
  .skill-group:nth-child(3) .skill-pct { color: var(--gold); }

  .skill-bar {
    height: 5px;
    background: rgba(255,255,255,0.1);
    border-radius: 3px;
    overflow: hidden;
  }

  .skill-fill {
    height: 100%;
    border-radius: 3px;
    transform-origin: left;
    animation: barGrow 1s 0.5s ease both;
  }

  .skill-group:nth-child(1) .skill-fill { background: var(--coral); }
  .skill-group:nth-child(2) .skill-fill { background: var(--teal); }
  .skill-group:nth-child(3) .skill-fill { background: var(--gold); }

  /* ── EDUCATION ── */
  .education { background: white; }

  .edu-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 28px;
  }

  .edu-card {
    border-radius: 24px;
    padding: 36px 32px;
    position: relative;
    overflow: hidden;
    transition: transform 0.3s;
  }

  .edu-card:hover { transform: translateY(-4px); }

  .edu-card:nth-child(1) { background: linear-gradient(135deg, rgba(255,107,107,0.08), rgba(255,107,107,0.02)); border: 1px solid rgba(255,107,107,0.15); }
  .edu-card:nth-child(2) { background: linear-gradient(135deg, rgba(46,196,182,0.08), rgba(46,196,182,0.02)); border: 1px solid rgba(46,196,182,0.15); }
  .edu-card:nth-child(3) { background: linear-gradient(135deg, rgba(107,45,139,0.08), rgba(107,45,139,0.02)); border: 1px solid rgba(107,45,139,0.15); }
  .edu-card:nth-child(4) { background: linear-gradient(135deg, rgba(255,179,71,0.08), rgba(255,179,71,0.02)); border: 1px solid rgba(255,179,71,0.15); }

  .edu-icon { font-size: 36px; margin-bottom: 18px; }

  .edu-degree {
    font-family: 'Playfair Display', serif;
    font-size: 19px;
    font-weight: 700;
    margin-bottom: 6px;
    color: var(--dark);
  }

  .edu-school {
    font-size: 14px;
    color: var(--mid);
    font-weight: 500;
    margin-bottom: 8px;
  }

  .edu-year {
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 1.5px;
    text-transform: uppercase;
  }

  .edu-card:nth-child(1) .edu-year { color: var(--coral); }
  .edu-card:nth-child(2) .edu-year { color: var(--teal); }
  .edu-card:nth-child(3) .edu-year { color: var(--plum); }
  .edu-card:nth-child(4) .edu-year { color: #b87c00; }

  /* ── CONTACT ── */
  .contact {
    background: linear-gradient(135deg, var(--plum) 0%, var(--dark) 50%, #0f3460 100%);
    padding: 120px 0;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .contact::before {
    content: '';
    position: absolute;
    width: 500px; height: 500px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(46,196,182,0.2) 0%, transparent 70%);
    top: -200px; left: -100px;
  }

  .contact::after {
    content: '';
    position: absolute;
    width: 400px; height: 400px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(255,107,107,0.15) 0%, transparent 70%);
    bottom: -150px; right: 0;
  }

  .contact .container { position: relative; z-index: 2; }

  .contact-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(36px, 5vw, 56px);
    font-weight: 900;
    color: white;
    margin-bottom: 20px;
  }

  .contact-sub {
    font-size: 16px;
    color: rgba(255,255,255,0.65);
    max-width: 480px;
    margin: 0 auto 48px;
    line-height: 1.7;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
  }

  .contact-btn {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 14px 28px;
    border-radius: 50px;
    font-size: 14px;
    font-weight: 600;
    text-decoration: none;
    transition: all 0.3s;
    cursor: pointer;
  }

  .contact-btn.primary {
    background: var(--coral);
    color: white;
    box-shadow: 0 8px 24px rgba(255,107,107,0.4);
  }

  .contact-btn.primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 14px 32px rgba(255,107,107,0.5);
  }

  .contact-btn.secondary {
    background: rgba(255,255,255,0.1);
    color: white;
    border: 1px solid rgba(255,255,255,0.2);
    backdrop-filter: blur(8px);
  }

  .contact-btn.secondary:hover {
    background: rgba(255,255,255,0.18);
    transform: translateY(-3px);
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-8px); }
  }

  @keyframes barGrow {
    from { transform: scaleX(0); }
    to { transform: scaleX(1); }
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    .hero { grid-template-columns: 1fr; min-height: auto; }
    .hero-right { display: none; }
    .hero-left { padding: 60px 32px; }
    .about-grid, .skills-grid, .edu-grid { grid-template-columns: 1fr; }
    .exp-card { grid-template-columns: 1fr; }
    .container { padding: 0 24px; }
    section { padding: 70px 0; }
  }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="hero-left">
    <span class="hero-tag">Open to Opportunities</span>
    <h1 class="hero-name">Rica Mae<br><span>Dominguez</span></h1>
    <p class="hero-subtitle">IT Specialist · Web Manager · Program Coordinator — bridging enterprise tech support, digital communications, and advocacy from Quezon City, Philippines.</p>
    <div class="hero-roles">
      <span class="role-pill">🖥 Enterprise IT Support</span>
      <span class="role-pill">🌐 WordPress / Elementor</span>
      <span class="role-pill">🎨 Canva Design</span>
      <span class="role-pill">📋 Program Coordination</span>
      <span class="role-pill">🗣 English · Filipino · Spanish</span>
    </div>
  </div>
  <div class="hero-right">
    <div class="hero-visual">
      <div class="avatar-card">
        <div class="avatar-initials">RMD</div>
        <div class="avatar-label">Portfolio 2026</div>
      </div>
      <div class="float-badge b1">
        <span class="badge-emoji">🏛</span>
        <div class="badge-text">History Grad · PUP</div>
      </div>
      <div class="float-badge b2">
        <span class="badge-emoji">💻</span>
        <div class="badge-text">IT Specialist II</div>
      </div>
      <div class="float-badge b3">
        <span class="badge-emoji">🌿</span>
        <div class="badge-text">Foundation Work</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="about">
  <div class="container">
    <div class="section-label"><span></span><span>About Me</span></div>
    <div class="about-grid">
      <div class="about-text">
        <h2 class="section-title">A little bit of<br><em>everything</em> — intentionally.</h2>
        <p>I'm Rica, an IT Specialist II at <strong>Stefanini Philippines</strong> and Program Coordinator at <strong>Constantino Foundation</strong> — a nonprofit dedicated to progressive historical and social advocacy.</p>
        <p>With over a decade of professional experience across IT support, customer service, sales, event production, and program coordination, I bring a rare combination of technical depth and organizational versatility. I resolve complex enterprise incidents, manage knowledge bases, and mentor teams — while also building websites and running advocacy programs on the side.</p>
        <p>I'm largely <strong>self-taught in web and design</strong> — I learned by exploring, dragging, dropping, and figuring things out. I believe curiosity and persistence are often better teachers than formal training.</p>
      </div>
      <div class="stats-grid">
        <div class="stat-card">
          <div class="stat-num">10+</div>
          <div class="stat-label">Years Professional Experience</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">6</div>
          <div class="stat-label">Industries & Roles</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">2</div>
          <div class="stat-label">Websites Managed</div>
        </div>
        <div class="stat-card">
          <div class="stat-num">3</div>
          <div class="stat-label">Languages Spoken</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section class="experience">
  <div class="container">
    <div class="section-label"><span></span><span>Experience</span></div>
    <h2 class="section-title">Where I've been<br>doing the work.</h2>
    <div class="exp-timeline">

      <div class="exp-card">
        <div class="exp-icon">💻</div>
        <div>
          <div class="exp-period">OCT 2022 – FEB 2026 · STEFANINI PHILIPPINES</div>
          <div class="exp-title">IT Specialist II</div>
          <div class="exp-company">Stefanini Philippines · Work from Home</div>
          <div class="exp-desc">Served as subject matter expert on client-specific tools, programs, and applications. Resolved end-user requests and incidents via ServiceNow, Globys, Webbing, and Fivestar — managing ticket queues, monitoring system performance, and ensuring timely service delivery. Diagnosed Outlook/Exchange issues, coordinated with global IT support teams, and acted as go-to escalation resource for complex issues. Maintained and updated KB articles for first-level support accuracy, mentored team members, and led continuous improvement initiatives.</div>
          <div class="exp-tags">
            <span class="exp-tag">ServiceNow</span>
            <span class="exp-tag">Outlook / Exchange</span>
            <span class="exp-tag">Globys · Webbing · Fivestar</span>
            <span class="exp-tag">KB Management</span>
            <span class="exp-tag">Team Mentoring</span>
            <span class="exp-tag">Escalation Handling</span>
          </div>
        </div>
      </div>

      <div class="exp-card">
        <div class="exp-icon">🌿</div>
        <div>
          <div class="exp-period">JAN 15, 2025 · CONSULTANCY AGREEMENT</div>
          <div class="exp-title">Program Coordinator</div>
          <div class="exp-company">Constantino Foundation · 38 Panay Avenue, Bgy. Paligsahan, Quezon City</div>
          <div class="exp-desc">Under a formal consultancy agreement, coordinate the Foundation's programs and events including the Lectures and Provocations series at Linangan Gallery, covering history-linked and transdisciplinary subjects. Manage the Foundation's social media accounts (Instagram, Facebook, BlueSky) including boosting, handle media and communications including newsletters and press work, and develop and maintain the WordPress website. Coordinate book publishing projects including the special 50th anniversary edition of <em>The Philippines: A Past Revisited</em> and the English translation of Virgilio Almario's <em>Panitikan ng Rebolusyong 1896</em>. Manage the director's calendar and appointments.</div>
          <div class="exp-tags">
            <span class="exp-tag">WordPress</span>
            <span class="exp-tag">Avada Builder</span>
            <span class="exp-tag">Social Media Management</span>
            <span class="exp-tag">Event Coordination</span>
            <span class="exp-tag">Book Publishing</span>
            <span class="exp-tag">PR & Communications</span>
            <span class="exp-tag">Canva</span>
          </div>
        </div>
      </div>

      <div class="exp-card">
        <div class="exp-icon">🦅</div>
        <div>
          <div class="exp-period">WEB PROJECT · ONGOING</div>
          <div class="exp-title">Website Creator & Manager</div>
          <div class="exp-company">Alas Ng Bayan · Quezon City</div>
          <div class="exp-desc">Built and manage the Alas Ng Bayan website independently using Elementor, without formal web development training. Handles layout design, content updates, and overall site maintenance through self-directed learning.</div>
          <div class="exp-tags">
            <span class="exp-tag">Elementor</span>
            <span class="exp-tag">WordPress</span>
            <span class="exp-tag">Content Management</span>
            <span class="exp-tag">Self-Taught</span>
          </div>
        </div>
      </div>

      <div class="exp-card exp-card-4">
        <div class="exp-icon">🍎</div>
        <div>
          <div class="exp-period">MAR 2021 – AUG 2022 · CONCENTRIX DAKSH, QC</div>
          <div class="exp-title">Sales Advisor <span style="font-weight:400;font-size:14px;color:var(--mid)">(formerly Technical & Media Services Advisor)</span></div>
          <div class="exp-company">Concentrix Daksh · Quezon City</div>
          <div class="exp-desc">Started as a Technical and Media Services Advisor providing technical and media service support, then advanced to Sales Advisor recommending products and solutions for customer needs. Resolved customer inquiries and complaints efficiently. Skilled in Salesforce, Core, iCloud Support Tool, and Apple MZ Support.</div>
          <div class="exp-tags">
            <span class="exp-tag">Salesforce</span>
            <span class="exp-tag">iCloud Support Tool</span>
            <span class="exp-tag">Apple MZ Support</span>
            <span class="exp-tag">Technical Support</span>
            <span class="exp-tag">Sales</span>
          </div>
        </div>
      </div>

      <div class="exp-card exp-card-5">
        <div class="exp-icon">🎧</div>
        <div>
          <div class="exp-period">OCT 2019 – JAN 2021 · TELEPERFORMANCE PHILIPPINES, QC</div>
          <div class="exp-title">Customer Service Specialist</div>
          <div class="exp-company">Teleperformance Philippines · Quezon City</div>
          <div class="exp-desc">Delivered customer assistance through phone, email, and platform queries. Handled billing, payment, and delivery disputes while maintaining accurate records. Specialist in Salesforce, Dispatch, and Okta tools.</div>
          <div class="exp-tags">
            <span class="exp-tag">Salesforce</span>
            <span class="exp-tag">Okta</span>
            <span class="exp-tag">Dispatch</span>
            <span class="exp-tag">Customer Support</span>
          </div>
        </div>
      </div>

      <div class="exp-card exp-card-6">
        <div class="exp-icon">🎵</div>
        <div>
          <div class="exp-period">MAY 2016 – 2018 · FREELANCE</div>
          <div class="exp-title">Production Coordinator</div>
          <div class="exp-company">Freelance · Metro Manila</div>
          <div class="exp-desc">Coordinated concerts, festivals, and brand activation events — managing logistics, registrations, and program flow. Supported on-site production for international and local artists, corporate events, and media launches. Partnered with Billboard Philippines, Bandwagon Asia, and local event agencies. Notable events: Microsoft Azure Summit: Mission 313 (Sofitel Manila, 2018), Erykah Badu vs. Everythang Tour (Sofitel Manila, 2017), AkzoNobel Philippines (Dusit Thani Makati, 2018), Bandwagon Music Market Festival (Circuit Makati, 2016).</div>
          <div class="exp-tags">
            <span class="exp-tag">Event Production</span>
            <span class="exp-tag">Logistics</span>
            <span class="exp-tag">Billboard Philippines</span>
            <span class="exp-tag">Bandwagon Asia</span>
            <span class="exp-tag">Corporate Events</span>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- SKILLS -->
<section class="skills">
  <div class="container">
    <div class="section-label"><span></span><span>Skills</span></div>
    <h2 class="section-title">Tools & capabilities<br>I work with daily.</h2>
    <div class="skills-grid">

      <div class="skill-group">
        <div class="skill-group-icon">🖥</div>
        <div class="skill-group-title">IT & Technical</div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">ServiceNow / Ticketing</span><span class="skill-pct">90%</span></div><div class="skill-bar"><div class="skill-fill" style="width:90%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Outlook / Exchange</span><span class="skill-pct">85%</span></div><div class="skill-bar"><div class="skill-fill" style="width:85%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Salesforce / Okta</span><span class="skill-pct">85%</span></div><div class="skill-bar"><div class="skill-fill" style="width:85%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Technical Troubleshooting</span><span class="skill-pct">88%</span></div><div class="skill-bar"><div class="skill-fill" style="width:88%"></div></div></div>
      </div>

      <div class="skill-group">
        <div class="skill-group-icon">🌐</div>
        <div class="skill-group-title">Web Management</div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">WordPress</span><span class="skill-pct">80%</span></div><div class="skill-bar"><div class="skill-fill" style="width:80%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Elementor</span><span class="skill-pct">78%</span></div><div class="skill-bar"><div class="skill-fill" style="width:78%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Avada Theme Builder</span><span class="skill-pct">75%</span></div><div class="skill-bar"><div class="skill-fill" style="width:75%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Hostinger / Hosting</span><span class="skill-pct">70%</span></div><div class="skill-bar"><div class="skill-fill" style="width:70%"></div></div></div>
      </div>

      <div class="skill-group">
        <div class="skill-group-icon">🎨</div>
        <div class="skill-group-title">Design & Coordination</div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Canva (Graphic Design)</span><span class="skill-pct">88%</span></div><div class="skill-bar"><div class="skill-fill" style="width:88%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Program Coordination</span><span class="skill-pct">85%</span></div><div class="skill-bar"><div class="skill-fill" style="width:85%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Research & Documentation</span><span class="skill-pct">90%</span></div><div class="skill-bar"><div class="skill-fill" style="width:90%"></div></div></div>
        <div class="skill-item"><div class="skill-row"><span class="skill-name">Social Media Content</span><span class="skill-pct">80%</span></div><div class="skill-bar"><div class="skill-fill" style="width:80%"></div></div></div>
      </div>

    </div>
  </div>
</section>

<!-- EDUCATION -->
<section class="education">
  <div class="container">
    <div class="section-label"><span></span><span>Education & Background</span></div>
    <h2 class="section-title">Shaped by different<br>fields of learning.</h2>
    <div class="edu-grid">
      <div class="edu-card">
        <div class="edu-icon">🏛</div>
        <div class="edu-degree">Bachelor of Arts in History</div>
        <div class="edu-school">Polytechnic University of the Philippines</div>
        <div class="edu-year">2011 – 2016</div>
      </div>
      <div class="edu-card">
        <div class="edu-icon">⚖️</div>
        <div class="edu-degree">Juris Doctor (2 Semesters)</div>
        <div class="edu-school">Polytechnic University of the Philippines</div>
        <div class="edu-year">2020 – 2021</div>
      </div>
      <div class="edu-card">
        <div class="edu-icon">🌐</div>
        <div class="edu-degree">Web Management</div>
        <div class="edu-school">Self-Taught · WordPress, Avada, Elementor, Hostinger</div>
        <div class="edu-year">Ongoing · Practical Experience</div>
      </div>
      <div class="edu-card">
        <div class="edu-icon">🗣</div>
        <div class="edu-degree">Languages</div>
        <div class="edu-school">English (Fluent) · Filipino (Fluent) · Spanish (Elementary)</div>
        <div class="edu-year">Multilingual</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact">
  <div class="container">
    <h2 class="contact-title">Let's work together.</h2>
    <p class="contact-sub">I'm open to IT roles, web management projects, and coordination work. Feel free to reach out!</p>
    <div class="contact-links">
      <a class="contact-btn primary" href="mailto:rica.dominguez@gmail.com">✉️ rica.dominguez@gmail.com</a>
      <a class="contact-btn secondary" href="tel:+639985309247">📞 +63 9985 309 247</a>
      <a class="contact-btn secondary" href="https://www.constantinofoundation.org" target="_blank">🌐 Constantino Foundation</a>
    </div>
    <p style="color:rgba(255,255,255,0.35); font-size:13px; margin-top:48px;">Camarin, Caloocan City · Open to remote & on-site opportunities</p>
  </div>
</section>

</body>
</html>
