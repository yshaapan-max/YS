<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>YS Concierge | Youssef Shaaban</title>
  <meta name="description" content="Concierge services for high-net-worth individuals: premium international flights, ground transportation, and luxury accommodation." />
  <style>
    :root{
      --bg:#F4F9FF;
      --panel:#FFFFFF;
      --panel2:#F0F6FF;
      --text:#0B2A4A;
      --muted:#5B7FA6;
      --line:rgba(11,42,74,.12);
      --blue:#3AA0FF;
      --blue2:#7CC4FF;
      --shadow: 0 18px 40px rgba(58,160,255,.18);
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      color:var(--text);
      background:
        radial-gradient(1200px 700px at 20% -10%, rgba(122,196,255,.35), transparent 55%),
        radial-gradient(900px 600px at 85% 10%, rgba(58,160,255,.25), transparent 55%),
        linear-gradient(180deg, var(--bg), #EAF3FF);
    }
    a{color:inherit;text-decoration:none}
    .container{max-width:1100px;margin:0 auto;padding:28px}
    .nav{
      display:flex;align-items:center;justify-content:space-between;gap:18px;
      position:sticky;top:0;backdrop-filter:saturate(140%) blur(10px);
      background:rgba(7,10,18,.55);
      border-bottom:1px solid var(--line);
      padding:16px 28px;
      z-index:5;
    }
    .brand{display:flex;align-items:center;gap:12px}
    .mark{
      width:34px;height:34px;border-radius:12px;
      background:linear-gradient(135deg, rgba(58,160,255,.95), rgba(124,196,255,.85));
      position:relative;
      box-shadow:0 12px 30px rgba(58,160,255,.22);
      overflow:hidden;
    }
    .mark::after{
      content:"";
      position:absolute;inset:0;
      background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Cpath d='M6 35c13-10 27-13 52-14' fill='none' stroke='%230B2A4A' stroke-opacity='.25' stroke-width='4' stroke-linecap='round'/%3E%3Cpath d='M36 18l7 7-10 3' fill='none' stroke='%230B2A4A' stroke-opacity='.25' stroke-width='4' stroke-linecap='round' stroke-linejoin='round'/%3E%3Cpath d='M34 26l10 6' fill='none' stroke='%230B2A4A' stroke-opacity='.25' stroke-width='4' stroke-linecap='round'/%3E%3C/svg%3E");
      background-size:70% 70%;
      background-repeat:no-repeat;
      background-position:center;
    }
    .brand-title{font-weight:800;letter-spacing:.3px;line-height:1.1}
    .brand-sub{font-size:12px;color:var(--muted)}
    .navlinks{display:flex;gap:14px;flex-wrap:wrap;justify-content:flex-end}
    .navlinks a{opacity:.9;font-size:14px}
    .navlinks a:hover{opacity:1}

    .btn{
      display:inline-flex;align-items:center;justify-content:center;gap:10px;
      padding:12px 16px;border-radius:14px;
      border:1px solid rgba(214,177,94,.35);
      font-weight:750;letter-spacing:.2px;
      transition:transform .12s ease, background .12s ease, border-color .12s ease;
    }
    .btn:hover{transform:translateY(-1px)}
    .btn.primary{
      background:linear-gradient(135deg, var(--blue), var(--blue2));
      color:#06325C;
      border-color:rgba(58,160,255,.55);
      box-shadow:0 14px 40px rgba(58,160,255,.28);
    }
    .btn.secondary{background:rgba(255,255,255,.04)}
    .btn.small{padding:10px 12px;border-radius:12px;font-size:14px}

    .hero{
      display:grid;grid-template-columns:1.2fr .8fr;gap:18px;align-items:stretch;
      padding:42px 0 12px;
      position:relative;
    }
    .hero::before{
      content:"";
      position:absolute;
      inset:-40px -20px auto -20px;
      height:260px;
      background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1200 300'%3E%3Cpath d='M40 210 C 240 70, 420 70, 620 170 S 980 290, 1160 140' fill='none' stroke='%233AA0FF' stroke-opacity='.12' stroke-width='6' stroke-linecap='round'/%3E%3Cpath d='M720 120 l18 18 -26 7' fill='none' stroke='%233AA0FF' stroke-opacity='.12' stroke-width='6' stroke-linecap='round' stroke-linejoin='round'/%3E%3Cpath d='M710 145 l26 15' fill='none' stroke='%233AA0FF' stroke-opacity='.12' stroke-width='6' stroke-linecap='round'/%3E%3C/svg%3E");
      background-repeat:no-repeat;
      background-size:cover;
      pointer-events:none;
    }
    .tag{
      display:inline-flex;align-items:center;gap:10px;
      padding:8px 12px;border-radius:999px;
      border:1px solid rgba(214,177,94,.35);
      background:rgba(214,177,94,.10);
      color:var(--gold2);
      font-size:13px;
    }
    h1{font-size:48px;line-height:1.03;margin:14px 0 12px;letter-spacing:-.6px}
    .lead{color:var(--muted);line-height:1.65;font-size:16px;margin:0}
    .hero-actions{display:flex;gap:10px;flex-wrap:wrap;margin-top:18px}

    .card{
      background:linear-gradient(180deg, #FFFFFF, #F3F8FF);
      border:1px solid var(--line);
      border-radius:22px;
      padding:18px;
      box-shadow:var(--shadow);
    }
    .card h3{margin:0 0 8px;font-size:18px}
    .muted{color:var(--muted)}

    .kpis{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:18px}
    .kpi{padding:14px;border-radius:18px;border:1px solid var(--line);background:rgba(255,255,255,.03)}
    .kpi strong{font-size:20px}

    .section{margin-top:34px}
    .section h2{margin:0 0 10px;font-size:28px;letter-spacing:-.2px}

    .grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
    .grid2{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}

    .service{padding:16px;border-radius:20px;border:1px solid var(--line);background:rgba(255,255,255,.03)}
    .service .title{display:flex;align-items:center;gap:10px;margin-bottom:6px}
    .dot{width:10px;height:10px;border-radius:999px;background:linear-gradient(135deg, var(--gold), var(--gold2))}

    .list{margin:10px 0 0;padding:0;list-style:none}
    .list li{padding:10px 0;border-top:1px solid rgba(255,255,255,.08);color:var(--muted)}
    .list li:first-child{border-top:0;padding-top:0}

    .process{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}
    .step{padding:14px;border-radius:20px;border:1px solid var(--line);background:rgba(255,255,255,.03)}
    .step .num{display:inline-flex;align-items:center;justify-content:center;width:30px;height:30px;border-radius:12px;
      background:rgba(214,177,94,.14);border:1px solid rgba(214,177,94,.32);color:var(--gold2);font-weight:800;margin-bottom:10px}

    .testimonial{padding:16px;border-radius:20px;border:1px solid var(--line);background:rgba(255,255,255,.03)}
    .quote{color:var(--muted);line-height:1.65;margin:0 0 10px}
    .who{font-weight:800}

    .contact{
      display:grid;grid-template-columns:1fr 1fr;gap:12px
    }
    label{display:block;font-size:13px;color:var(--muted);margin:0 0 6px}

    .portrait{
      width:112px;height:112px;
      border-radius:22px;
      object-fit:cover;
      border:2px solid rgba(58,160,255,.35);
      box-shadow:0 14px 36px rgba(58,160,255,.22);
      filter:grayscale(1) contrast(1.05);
      transition:filter .18s ease, transform .18s ease;
      background:var(--panel2);
    }
    .portrait:hover{filter:grayscale(0) contrast(1.02);transform:translateY(-1px)}
    input, textarea{
      width:100%;padding:12px 12px;border-radius:14px;
      border:1px solid rgba(255,255,255,.14);
      background:#0A0F20;color:var(--text);
      outline:none;
    }
    textarea{min-height:130px;resize:vertical}
    .hint{font-size:12px;color:var(--muted);margin-top:10px;line-height:1.4}

    .footer{
      margin-top:40px;padding:18px 0 40px;
      color:var(--muted);
      border-top:1px solid rgba(255,255,255,.08);
      font-size:13px;
      display:flex;gap:14px;flex-wrap:wrap;justify-content:space-between;align-items:center
    }
    .pill{display:inline-flex;align-items:center;gap:8px;padding:9px 12px;border-radius:999px;border:1px solid var(--line);background:rgba(255,255,255,.03)}

    @media (max-width: 980px){
      .hero{grid-template-columns:1fr}
      h1{font-size:40px}
      .kpis{grid-template-columns:1fr}
      .grid3,.grid2{grid-template-columns:1fr}
      .process{grid-template-columns:1fr 1fr}
      .contact{grid-template-columns:1fr}
      .nav{position:relative;top:auto}
    }
    @media (max-width: 520px){
      .process{grid-template-columns:1fr}
      h1{font-size:36px}
      .nav{padding:14px 16px}
    }
      h1{font-size:36px}
      .nav{padding:14px 16px}
    }
  </style>
</head>
<body>
  <header class="nav">
    <div class="brand">
      <div class="mark" aria-hidden="true"></div>
      <div>
        <div class="brand-title">YS Concierge</div>
        <div class="brand-sub">Youssef Shaaban</div>
      </div>
    </div>

    <nav class="navlinks" aria-label="Primary">
      <a href="#services">Services</a>
      <a href="#process">Process</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
      <a class="btn small secondary" href="tel:+201228204344">Call</a>
    </nav>
  </header>

  <main class="container">
    <section class="hero" id="top">
      <div>
        <span class="tag">Private Aviation & Travel Concierge • Discreet • Fast response</span>
        <h1>Concierge services for high‑net‑worth clients — travel handled end‑to‑end.</h1>
        <p class="lead">
          I support clients with <strong>Business & First Class international travel</strong>, <strong>chauffeured ground transportation</strong>, and <strong>premium accommodation coordination</strong> — delivered with speed, accuracy, and discretion.
        </p>

        <div class="hero-actions">
          <a class="btn primary" href="#contact">Request Concierge Support</a>
          <a class="btn secondary" href="https://wa.me/201228204344" target="_blank" rel="noreferrer">WhatsApp</a>
          <a class="btn secondary" href="mailto:yshaapan@gmail.com">Email</a>
        </div>

        <div class="kpis" aria-label="Key highlights">
          <div class="kpi">
            <strong>VIP-first</strong>
            <div class="muted">White-glove handling and proactive updates</div>
          </div>
          <div class="kpi">
            <strong>Global</strong>
            <div class="muted">International itineraries and multi-city planning</div>
          </div>
          <div class="kpi">
            <strong>Discreet</strong>
            <div class="muted">Confidentiality and attention to detail</div>
          </div>
        </div>
      </div>

      <aside class="card" aria-label="Quick contact">
        <div style="display:flex;gap:14px;align-items:center;margin-bottom:14px">
          <img src="data:image/jpeg;base64,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" alt="Youssef Shaaban" class="portrait" />
          <div>
            <strong style="font-size:18px">Youssef Shaaban</strong>
            <div class="muted" style="margin-top:4px">Private Aviation & Travel Concierge</div>
          </div>
        </div>
        <h3>Direct Contact</h3>
        <p class="muted" style="margin:0 0 14px;line-height:1.55">
          Prefer direct coordination? Reach me anytime using the options below.
        </p>
        <div style="display:grid;gap:10px">
          <span class="pill"><strong>Phone:</strong> <a href="tel:+201228204344">01228204344</a></span>
          <span class="pill"><strong>Email:</strong> <a href="mailto:yshaapan@gmail.com">yshaapan@gmail.com</a></span>
          <span class="pill"><strong>WhatsApp:</strong> <a href="https://wa.me/201228204344" target="_blank" rel="noreferrer">Chat on WhatsApp</a></span>
        </div>
        <p class="hint">
          Availability and response times can vary by time zone. For urgent travel issues, WhatsApp is typically fastest.
        </p>
      </aside>
    </section>

    <section class="section" id="services">
      <h2>Services</h2>
      <p class="muted" style="margin:0 0 14px;line-height:1.6">
        Concierge support tailored to busy executives and high‑net‑worth individuals.
      </p>

      <div class="grid3">
        <div class="service">
          <div class="title"><span class="dot"></span><strong>Business & First Class Flights</strong></div>
          <div class="muted">International bookings, complex routings, and preferred options when available.</div>
          <ul class="list">
            <li>Multi‑city itinerary planning</li>
            <li>Fare monitoring & alternative options</li>
            <li>Travel-ready documentation checklist</li>
          </ul>
        </div>
        <div class="service">
          <div class="title"><span class="dot"></span><strong>Ground Transportation</strong></div>
          <div class="muted">Airport transfers, chauffeur requests, and coordinated pickup/drop‑off.</div>
          <ul class="list">
            <li>Seamless coordination and timing</li>
            <li>Special requests where applicable</li>
            <li>City-to-city transport support</li>
          </ul>
        </div>
        <div class="service">
          <div class="title"><span class="dot"></span><strong>Accommodation</strong></div>
          <div class="muted">Hotel selection support with convenience, location, and client preferences in mind.</div>
          <ul class="list">
            <li>Short‑stay and extended stays</li>
            <li>Preference-based recommendations</li>
            <li>Request handling and follow-up</li>
          </ul>
        </div>
      </div>

      <div class="card" style="margin-top:12px">
        <h3 style="margin:0 0 8px">Other requests</h3>
        <p class="muted" style="margin:0;line-height:1.6">
          If you have a request not listed above, reach out — I can often coordinate solutions or recommend the next best step.
        </p>
      </div>
    </section>

    <section class="section" id="process">
      <h2>How it works</h2>
      <p class="muted" style="margin:0 0 14px;line-height:1.6">A simple process designed for speed and clarity.</p>
      <div class="process">
        <div class="step">
          <div class="num">1</div>
          <strong>Request</strong>
          <div class="muted" style="margin-top:6px;line-height:1.55">Send your details (dates, route, preferences, budget range).</div>
        </div>
        <div class="step">
          <div class="num">2</div>
          <strong>Options</strong>
          <div class="muted" style="margin-top:6px;line-height:1.55">I return curated options with clear breakdowns and tradeoffs.</div>
        </div>
        <div class="step">
          <div class="num">3</div>
          <strong>Confirm</strong>
          <div class="muted" style="margin-top:6px;line-height:1.55">You approve the selection and I proceed with booking/coordination.</div>
        </div>
        <div class="step">
          <div class="num">4</div>
          <strong>Support</strong>
          <div class="muted" style="margin-top:6px;line-height:1.55">Ongoing assistance for changes and travel-day coordination.</div>
        </div>
      </div>
    </section>

    <section class="section" id="about">
      <h2>About</h2>
      <div class="grid2">
        <div class="card">
          <h3>Youssef Shaaban</h3>
          <p class="muted" style="margin:0;line-height:1.7">
            I provide private concierge-style travel coordination for clients who value discretion, speed, and premium outcomes.
            My work is built around efficiency: fewer messages, clearer options, and confident execution — so your travel runs smoothly.
          </p>
          <div style="display:flex;gap:10px;flex-wrap:wrap;margin-top:14px">
            <a class="btn secondary" href="mailto:yshaapan@gmail.com">yshaapan@gmail.com</a>
            <a class="btn secondary" href="tel:+201228204344">01228204344</a>
          </div>
        </div>
        <div class="card">
          <h3>Client experience</h3>
          <p class="muted" style="margin:0 0 10px;line-height:1.7">
            The goal is to keep things effortless on your side — clear communication, confirmed details, and proactive updates.
          </p>
          <ul class="list">
            <li>Professional, prompt communication</li>
            <li>Preference-driven recommendations</li>
            <li>Attention to details (timings, connections, notes)</li>
          </ul>
        </div>
      </div>
    </section>

    <section class="section" aria-label="Testimonials">
      <h2>Client Notes</h2>
      <p class="muted" style="margin:0 0 14px;line-height:1.6">
        Replace these placeholders with real client feedback when ready.
      </p>
      <div class="grid3">
        <div class="testimonial">
          <p class="quote">“Everything was handled smoothly and quickly — I didn’t have to chase details.”</p>
          <div class="who">— Client, Executive Travel</div>
        </div>
        <div class="testimonial">
          <p class="quote">“Clear options, fast turnaround, and great attention to preferences.”</p>
          <div class="who">— Client, International Trips</div>
        </div>
        <div class="testimonial">
          <p class="quote">“Reliable support when plans changed last minute.”</p>
          <div class="who">— Client, Multi‑city Itinerary</div>
        </div>
      </div>
    </section>

    <section class="section" id="contact">
      <h2>Contact</h2>
      <p class="muted" style="margin:0 0 14px;line-height:1.6">
        Send your request and I’ll reply as soon as possible. If it’s urgent, WhatsApp is best.
      </p>

      <div class="contact">
        <div class="card">
          <h3>Send a message</h3>
          <form id="contactForm">
            <div style="display:grid;gap:10px">
              <div>
                <label for="name">Your name</label>
                <input id="name" name="name" placeholder="Name" required />
              </div>
              <div>
                <label for="email">Email</label>
                <input id="email" type="email" name="email" placeholder="name@example.com" required />
              </div>
              <div>
                <label for="message">What do you need help with?</label>
                <textarea id="message" name="message" placeholder="Dates, route, class, hotel preferences, pickup details, etc." required></textarea>
              </div>
              <button class="btn primary" type="submit" style="cursor:pointer">Send Email</button>
              <p class="hint">This form opens your email app (no domain needed). If you want a real web form later, I can add Formspree or another free form handler.</p>
            </div>
          </form>
        </div>

        <div class="card">
          <h3>Direct options</h3>
          <p class="muted" style="margin:0 0 14px;line-height:1.6">Choose the fastest way to reach me:</p>
          <div style="display:grid;gap:10px">
            <a class="btn secondary" href="tel:+201228204344">Call: 01228204344</a>
            <a class="btn secondary" href="mailto:yshaapan@gmail.com">Email: yshaapan@gmail.com</a>
            <a class="btn secondary" href="https://wa.me/201228204344" target="_blank" rel="noreferrer">WhatsApp: +20 122 820 4344</a>
          </div>
          <div class="card" style="margin-top:12px;background:rgba(255,255,255,.02)">
            <strong>What to include in your request</strong>
            <ul class="list">
              <li>Dates + departure/arrival cities</li>
              <li>Preferred cabin (Business/First)</li>
              <li>Traveler names exactly as passport</li>
              <li>Hotel location preferences and requirements</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <footer class="footer">
      <div>© <span id="year"></span> YS Concierge — Youssef Shaaban</div>
      <div style="display:flex;gap:10px;flex-wrap:wrap">
        <a class="pill" href="#top">Back to top</a>
        <a class="pill" href="mailto:yshaapan@gmail.com">Email</a>
        <a class="pill" href="tel:+201228204344">Call</a>
      </div>
    </footer>
  </main>

  <script>
    // No backend needed: this opens the user's email client with a pre-filled message.
    const form = document.getElementById('contactForm');
    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const message = document.getElementById('message').value.trim();
      const subject = encodeURIComponent('Concierge request');
      const body = encodeURIComponent(
        `Name: ${name}\nEmail: ${email}\n\nRequest:\n${message}\n\n— Sent from ysconcierge site`
      );
      window.location.href = `mailto:yshaapan@gmail.com?subject=${subject}&body=${body}`;
    });

    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
