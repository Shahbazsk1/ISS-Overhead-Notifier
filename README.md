<h1>🚀 ISS Overhead Notifier</h1>

    <h2>🔎 Description:</h2>
    <p>This Python-based project notifies you via email when the International Space Station (ISS) is passing over your location at night.
    It checks your geographical position against the current ISS coordinates and verifies if it's currently nighttime in your location.
    If both conditions are satisfied, an email alert is triggered to tell you to look up and try spotting the ISS in the night sky!</p>

    <h2>🧱 Modules and Libraries Used:</h2>

    <div class="module">
        <strong>1. requests</strong><br>
        <em>Purpose:</em> To send HTTP requests to public APIs (ISS position & sunrise/sunset info).<br>
        <a href="https://docs.python-requests.org" target="_blank">Official Docs</a>
    </div>

    <div class="module">
        <strong>2. datetime</strong><br>
        <em>Purpose:</em> To get the current hour to determine if it's night.
    </div>

    <div class="module">
        <strong>3. smtplib</strong><br>
        <em>Purpose:</em> To send an email notification using Gmail SMTP server.<br>
        <a href="https://docs.python.org/3/library/smtplib.html" target="_blank">SMTP Protocol Client Docs</a>
    </div>

    <div class="module">
        <strong>4. time</strong><br>
        <em>Purpose:</em> Adds a 60-second interval between checks to avoid too frequent requests and emails.
    </div>

    <h2>🌐 APIs Used:</h2>
    <ul>
        <li>
            <strong>ISS Position API:</strong>
            <a href="http://api.open-notify.org/iss-now.json" target="_blank">http://api.open-notify.org/iss-now.json</a>
        </li>
        <li>
            <strong>Sunrise-Sunset API:</strong>
            <a href="https://api.sunrise-sunset.org/json" target="_blank">https://api.sunrise-sunset.org/json</a>
        </li>
    </ul>
<h2>🌐 APIs Used</h2>

    <h3>1. ISS Position API</h3>
    <p><strong>URL:</strong> <a href="http://api.open-notify.org/iss-now.json" target="_blank">http://api.open-notify.org/iss-now.json</a></p>
    <p><strong>Purpose:</strong> Returns the current location of the ISS as latitude and longitude.</p>
    <p><strong>Sample Response:</strong></p>
    <pre><code>{
  "iss_position": {
    "latitude": "47.6062",
    "longitude": "-122.3321"
  },
  "timestamp": 1596567890,
  "message": "success"
}</code></pre>

    <h3>2. Sunrise-Sunset API</h3>
    <p><strong>URL:</strong> <a href="https://api.sunrise-sunset.org/json" target="_blank">https://api.sunrise-sunset.org/json</a></p>
    <p><strong>Purpose:</strong> Returns the sunrise and sunset times for a given location.</p>
    <p><strong>Sample Request:</strong></p>
    <pre><code>https://api.sunrise-sunset.org/json?lat=19.189300&amp;lng=73.02180&amp;formatted=0</code></pre>

    <p><strong>Sample Response:</strong></p>
    <pre><code>{
  "results": {
    "sunrise": "2025-07-23T00:44:32+00:00",
    "sunset": "2025-07-23T13:15:32+00:00",
    ...
  },
  "status": "OK"
}</code></pre>
