<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Insight On Investments — Clear Market Intelligence</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --blue-600: #0b6cff;   /* primary blue accent */
      --green-600: #1fb07b;  /* success/secondary green */
      --grey-100: #f4f6f8;   /* page background */
      --grey-700: #334155;   /* dark text */
      --glass: rgba(255,255,255,0.92);
      --card-border: rgba(16,40,60,0.06);
      --overlay: rgba(255,255,255,0.30); /* brightening overlay */
    }

    /* Reset */
    *{box-sizing:border-box;margin:0;padding:0}
    html,body{height:100%}
    body{
      font-family:"Inter",system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
      color:var(--grey-700);
      background:var(--grey-100);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
    }

    /* Background stock chart with Crypto logos (brightened) */
    .bg {
      position:fixed;
      inset:0;
      z-index:0;
      background-image: url("https://images.unsplash.com/photo-1518145784496-4267d9f0b2ee?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=00000000000000000000000000000000");
      background-size:cover;
      background-position:center;
      filter: contrast(1.05) saturate(1.05) brightness(1.18);
      transform: translateZ(0);
    }
    .bg::after{
      content:"";
      position:absolute;
      inset:0;
      background: linear-gradient(180deg, rgba(255,255,255,0.18), rgba(255,255,255,0.30));
      pointer-events:none;
    }

    /* Page container */
    .site {
      position:relative;
      z-index:2;
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:48px 20px;
    }

    .card {
      width:100%;
      max-width:1200px;
      background:var(--glass);
      border-radius:14px;
      padding:36px;
      box-shadow: 0 18px 40px rgba(20,40,60,0.12);
      border:1px solid var(--card-border);
      backdrop-filter: blur(6px) saturate(1.06);
    }

    header{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:18px;
      margin-bottom:22px;
    }
    .logo{
      font-weight:800;
      font-size:18px;
      color:var(--grey-700);
      letter-spacing:-0.4px;
    }
    nav a{
      margin-left:18px;
      color:var(--grey-700);
      font-weight:600;
      text-decoration:none;
      opacity:0.92;
    }

    .hero {
      display:grid;
      grid-template-columns: 1fr 380px;
      gap:28px;
      align-items:start;
    }

    /* Main heading */
    .hero h1{
      font-size: clamp(30px, 4.6vw, 48px);
      line-height:1.03;
      margin-bottom:14px;
      font-weight:800;
      color:var(--grey-700);
    }
    .lead{
      font-size:18px;
      color:#102233;
      margin-bottom:18px;
      font-weight:700;
      opacity:0.97;
    }

    /* Long explanatory copy area */
    .deep-explain {
      margin-top:12px;
      background: linear-gradient(180deg, rgba(11,108,255,0.04), rgba(31,176,123,0.02));
      padding:20px;
      border-radius:12px;
      border:1px solid rgba(10,20,40,0.03);
      color:#0e2a3a;
    }
    .deep-explain p{
      margin-bottom:12px;
      font-size:15.5px;
      color: #0f2a39;
      opacity:0.96;
    }
    .deep-explain strong{ font-weight:800; color:var(--grey-700); }

    /* Features grid */
    .features{
      margin-top:18px;
      display:grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap:12px;
    }
    .feature{
      background:white;
      padding:14px;
      border-radius:10px;
      border:1px solid rgba(8,18,30,0.04);
    }
    .feature h3{
      font-size:15px;
      font-weight:800;
      margin-bottom:8px;
      color:#043243;
    }
    .feature p{
      font-size:14px;
      color:#23414a;
    }

    /* Right column CTA and summary */
    .cta {
      display:flex;
      flex-direction:column;
      gap:14px;
    }
    .glass {
      background: linear-gradient(180deg, rgba(255,255,255,0.96), rgba(250,250,250,0.98));
      padding:18px;
      border-radius:12px;
      box-shadow: 0 8px 18px rgba(10,20,30,0.06);
      border:1px solid rgba(10,20,40,0.03);
    }
    .cta h3{ margin:0 0 8px 0; font-weight:800; color:var(--grey-700); }
    .cta p{ margin:0 0 12px 0; color:#173344; }

    .btn {
      display:inline-block;
      background: linear-gradient(90deg,var(--blue-600), #1466f0);
      color:white;
      padding:12px 16px;
      border-radius:10px;
      font-weight:800;
      text-decoration:none;
      text-align:center;
      box-shadow: 0 10px 26px rgba(11,108,255,0.16);
    }
    .btn-outline {
      display:inline-block;
      border:2px solid var(--green-600);
      color:var(--green-600);
      padding:10px 14px;
      border-radius:10px;
      font-weight:700;
      text-decoration:none;
      text-align:center;
    }

    footer{
      margin-top:20px;
      text-align:center;
      font-size:13px;
      color:#253a44;
      opacity:0.7;
    }

    /* Long-form sections below hero */
    .long-rows{
      margin-top:22px;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:18px;
    }
    .panel{
      background:#fff;
      padding:16px;
      border-radius:10px;
      border:1px solid rgba(8,18,30,0.04);
    }
    .panel h4{ font-size:15px; font-weight:800; margin-bottom:8px; color:#0a2a36; }
    .panel p{ font-size:14px; color:#243f49; margin-bottom:8px; }

    /* Responsive */
    @media (max-width:1000px){
      .hero{ grid-template-columns: 1fr; }
      .long-rows{ grid-template-columns: 1fr; }
      nav{ display:none; }
    }
  </style>
</head>
<body>
  <div class="bg" aria-hidden="true"></div>

  <div class="site">
    <div class="card">
      <header>
        <div class="logo">Insight On Investments</div>
        <nav>
          <a href="#how">How it helps</a>
          <a href="#features">Features</a>
          <a href="#start">Get Started</a>
        </nav>
      </header>

      <main class="hero">
        <section>
          <h1><strong>Actionable market intelligence with transparent reasoning.</strong> Trade and allocate with clarity, not guesswork.</h1>
          <p class="lead">
            Insight On Investments turns complex market behavior into clear guidance — combining automated signals, contextual analysis, and practical recommendations so you can make disciplined, repeatable decisions.
          </p>

          <div class="deep-explain" id="how" aria-labelledby="how-title">
            <h3 id="how-title" style="margin:0 0 10px 0; font-size:16px; font-weight:800;">How Insight On Investments helps you (long form)</h3>

            <p>
              Markets produce an enormous volume of information every second: price ticks, volume flows, sector rotations, macro surprises and news sentiment. Our platform ingests those streams, filters noise, and surfaces the patterns that matter for your objectives. We prioritize clarity: every signal is accompanied by a plain-English explanation, the data that produced it, and a concrete next step so you're not left guessing.
            </p>

            <p>
              We break value into three practical pillars:
            </p>
            <ul style="margin-left:18px; margin-bottom:12px;">
              <li><strong>Signal detection:</strong> Real-time scanning for technical setups, volatility shifts, volume surges and correlation breakouts tailored to your watchlists.</li>
              <li><strong>Contextual analysis:</strong> We layer macro environment, sector health, and recent news to explain whether a signal is likely to matter in the near term.</li>
              <li><strong>Execution-ready guidance:</strong> Position size suggestions, clear stop and target levels, and example trade entries so you can act consistently.</li>
            </ul>

            <p>
              We also provide learning moments: each recommendation includes a short rationale and a historical example that shows how similar setups behaved across different market regimes. This helps you understand not only "what" to do, but "why" and "when" to adjust.
            </p>

            <p style="margin-top:8px;">
              Whether you're active trader, a part-time investor, or an advisor managing client portfolios, Insight On Investments is designed to support disciplined, repeatable decision-making with transparency and practical tools.
            </p>
          </div>

          <div class="features" id="features">
            <div class="feature">
              <h3><strong>Customizable Alerts</strong></h3>
              <p>Define the exact triggers that matter to you — technical patterns, relative strength thresholds, or macro conditions — and receive prioritized, succinct alerts across email, SMS, or app push.</p>
            </div>
            <div class="feature">
              <h3><strong>Signal Explanations</strong></h3>
              <p>Every flag includes a short summary, the data that triggered it, a historical context paragraph, and suggested actions (entry, risk, and exit).</p>
            </div>
            <div class="feature">
              <h3><strong>Backtest & Scenario Tools</strong></h3>
              <p>Quick backtests and scenario analysis let you see how a strategy would have behaved in past bull, bear and sideways markets — with easy-to-read metrics and visual summaries.</p>
            </div>
            <div class="feature">
              <h3><strong>Risk Management</strong></h3>
              <p>Built-in sizing guidance, stop suggestions, and portfolio-level stress tests to quantify downside and avoid concentration risk.</p>
            </div>
          </div>

          <div class="long-rows" style="margin-top:18px;">
            <div class="panel">
              <h4>Who benefits most</h4>
              <p>Active traders who need concise, timely signals; investors who want market context before reallocating; advisors seeking reproducible rules for client portfolios.</p>
              <p>Our tools are optimized for people who prefer clear, action-focused recommendations — not opaque scores or raw data dumps.</p>
            </div>
            <div class="panel">
              <h4>Examples & Evidence</h4>
              <p>For each signal we provide a one-paragraph case study showing a prior occurrence, what followed, and a performance snapshot. This helps you calibrate expectations and understand edge & drawdown.</p>
              <p>We emphasize transparency: see the exact rules used for a signal, the lookback windows, and the historical outcomes by regime.</p>
            </div>
          </div>
        </section>

        <aside class="cta" aria-labelledby="cta-title">
          <div class="glass" role="region" aria-label="signup box">
            <h3 id="cta-title">Start with a prioritized market summary</h3>
            <p>
              Create a free account, add a watchlist, and receive a tailored market briefing within minutes — the top opportunities, the most urgent risks, and a succinct plan you can act on.
            </p>
            <a class="btn" href="#start">Create free account</a>
            <div style="margin-top:10px;">
              <a class="btn-outline" href="#learn">Request demo</a>
            </div>
          </div>

          <div style="font-size:13px; color:#0a2e36;">
          
          </div>
        </aside>
      </main>

      <footer>
        © <strong>Insight On Investments</strong> — Practical signals, clearly explained.
      </footer>
    </div>
  </div>

  <!-- Quick note: to use your own chart background, open the file and replace the URL in the .bg style rule at the top.
       Example console override:
       document.querySelector('.bg').style.backgroundImage = 'url("YOUR_IMAGE_URL")'
  -->
</body>
</html>
