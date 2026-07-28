# ampeop.github.io
A new way to explore the Stock Brokerage in live time while learning how to invest without the risk of losing your own cash!
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>AMP EOP — Learn to invest without risking your cash</title>
  <meta name="description" content="A new way to explore Stock Brokerage in real time while learning how to invest without the risk of losing your own cash!" />

  <!-- Open Graph for social previews -->
  <meta property="og:title" content="AMP EOP — Learn to invest without risking your cash" />
  <meta property="og:description" content="A new way to explore Stock Brokerage in real time while learning how to invest without the risk of losing your own cash!" />
  <meta property="og:image" content="https://source.unsplash.com/1200x630/?stock,finance,investing" />
  <meta property="og:type" content="website" />

  <!-- Google Font (optional) -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <a class="brand" href="/">AMP EOP</a>
      <nav class="nav">
        <a href="#features">Features</a>
        <a href="#howitworks">How it works</a>
        <a href="#signup" class="btn small">Get started</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" aria-labelledby="hero-title">
      <div class="container hero-grid">
        <div class="hero-copy">
          <h1 id="hero-title">Explore stock brokerage in real time — risk-free</h1>
          <p class="lead">A new way to explore Stock Brokerage in real time while learning how to invest without the risk of losing your own cash. Practice strategies, track performance, and build confidence before you invest.</p>
          <div class="hero-actions">
            <a href="#signup" class="btn primary">Try the demo</a>
            <a href="#features" class="btn ghost">See features</a>
          </div>

          <ul class="benefits">
            <li>Simulated trading with live market data</li>
            <li>Learning-focused dashboards & tutorials</li>
            <li>No real money required</li>
          </ul>
        </div>

        <figure class="hero-media" role="img" aria-label="Stock market chart on a laptop and mobile device">
          <!-- Unsplash source image (safe to replace with local asset) -->
          <img src="https://source.unsplash.com/900x700/?stock,finance,investing" alt="Stock charts and trading interface on a laptop screen" />
        </figure>
      </div>
    </section>

    <!-- Placeholder sections -->
    <section id="features" class="container section">...</section>
    <section id="howitworks" class="container section">...</section>
  </main>

  <footer class="site-footer">
    <div class="container">© <span id="year"></span> AMP EOP — Learn to invest, safely.</div>
  </footer>

  <script>
    // Update footer year
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
