<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Welcome</title>
  <style>
    /* --- Layout & Theme --- */
    body {
      margin: 0;
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif;
      background: #0f172a; /* slate-900 */
      color: #e5e7eb;      /* gray-200 */
      display: grid;
      place-items: center;
      min-height: 100vh;
      padding: 24px;
    }
    .wrap {
      width: 100%;
      max-width: 840px;
      background: #111827cc; /* glassy card */
      border: 1px solid #71809633;
      border-radius: 16px;
      overflow: hidden;
    }
    header {
      padding: 28px;
      text-align: center;
      border-bottom: 1px solid #71809633;
    }
    h1 { margin: 0; font-size: 34px; letter-spacing: .2px; }

    main {
      display: grid;
      gap: 20px;
      grid-template-columns: 1fr;
      padding: 22px;
    }
    @media (min-width: 820px) {
      main { grid-template-columns: 1.1fr 0.9fr; }
    }

    .card {
      background: #0b1220;
      border: 1px solid #71809633;
      border-radius: 12px;
      padding: 18px;
    }

    /* --- Wi‑Fi layout --- */
    .wifi {
      display: grid;
      grid-template-columns: 160px 1fr;
      gap: 18px;
      align-items: center;
    }
    @media (max-width: 560px) {
      .wifi { grid-template-columns: 1fr; text-align: center; }
    }
    .qr { background: #fff; padding: 12px; border-radius: 12px; display: inline-block; }
    .mono { font-family: ui-monospace, Menlo, Consolas, monospace; }

    /* --- Links & buttons (for the weather fallback link if needed) --- */
    a.button {
      display: inline-block;
      margin-top: 10px;
      padding: 10px 14px;
      border-radius: 10px;
      border: 1px solid #71809655;
      color: #e5e7eb;
      text-decoration: none;
      background: linear-gradient(180deg, rgba(96,165,250,.2), rgba(96,165,250,.08));
    }

    footer {
      text-align: center;
      padding: 12px 20px 20px;
      color: #94a3b8;
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <h1>Welcome</h1>
      <p>Please review the House Rules, check the local forecast, and connect to Wi‑Fi using the QR code.</p>
    </header>

    <main>
      <!-- House Rules (static text) -->
      <section class="card" id="house-rules">
        <h2>House Rules</h2>
        <div style="line-height:1.6">
          <p>Please take a moment to read these quick guidelines:</p>
          <ul style="margin-top:8px">
            <li>Quiet hours: 10:00 PM – 7:00 AM</li>
            <li>No smoking or vaping inside the unit</li>
            <li>Pets only with prior approval</li>
            <li>Trash &amp; recycling: use labeled bins in the hallway</li>
            <li>Check‑out: please load &amp; start the dishwasher, and place used towels in the hamper</li>
          </ul>
          <p style="margin-top:10px"><strong>Need anything?</strong> Text us and we’ll help right away.</p>
        </div>
      </section>

      <!-- Weather Forecast Widget (Columbus, GA) -->
      <section class="card" id="weather" style="margin-top:12px">
        <h2 style="margin-top:0">Columbus, GA Forecast</h2>

        <!-- WeatherWidget.io embed for Columbus, GA (5‑day forecast, US units) -->
        <a class="weatherwidget-io"
           href="https://forecast7.com/en/32d46n84d99/columbus/?unit=us"
           data-label_1="COLUMBUS"
           data-label_2="WEATHER"
           data-font="System UI"
           data-mode="Forecast"
           data-days="5"
           data-theme="original">Columbus Weather</a>

        <script>
          !function(d,s,id){
            var js, fjs = d.getElementsByTagName(s)[0];
            if(!d.getElementById(id)){
              js = d.createElement(s); js.id = id;
              js.src = 'https://weatherwidget.io/js/widget.min.js';
              fjs.parentNode.insertBefore(js, fjs);
            }
          }(document,'script','weatherwidget-io-js');
        </script>

        <!-- Fallback if scripts are blocked -->
        <noscript>
          <p>
            <a class="button" href="https://forecast.weather.gov/MapClick.php?lat=32.493197&lon=-84.892153"
               target="_blank" rel="noopener">
              View Columbus, GA forecast
            </a>
          </p>
        </noscript>
      </section>

      <!-- Wi‑Fi Access (uses a local PNG file named wifi_qr.png in the same folder) -->
      <section class="card" id="wifi">
        <h2>Wi‑Fi Access</h2>
        <div class="wifi">
          <div class="qr">
            <img src="wifi_qr.png" alt="Wi‑Fi QR code" width="160" height="160" />
          </div>
          <div>
            <p class="mono"><strong>Network (SSID):</strong> Unit 2B</p>
            <p class="mono"><strong>Password:</strong> abounds</p>
            <p class="mono"><strong>Security:</strong> WPA</p>
            <p style="color:#94a3b8">Tip: On iPhone/Android, open the Camera app and point it at the QR code to join.</p>
          </div>
        </div>
      </section>
    </main>

    <footer>© 2026 Welcome Page</footer>
  </div>
</body>
</html>
