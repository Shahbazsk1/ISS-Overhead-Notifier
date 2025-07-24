# 🌌 ISS Overhead Notifier
<h2>🔎 Description:</h2>
<p>This Python-based project notifies you via email when the International Space Station (ISS) is passing over your location at night. 
  It checks your geographical position against the current ISS coordinates and verifies if it's currently nighttime in your location. 
  If both conditions are satisfied, an email alert is triggered to tell you to look up and try spotting the ISS in the night sky!</p>
<h2>Modules and Libraries Used</h2>
<h3>1. requests</h3>
<ol>
  <li>requests
    <ul>
      <li>Purpose: To send HTTP requests to public APIs (ISS position & sunrise/sunset info).</li>
      <li><a href="https://docs.python-requests.org" target="_blank">https://docs.python-requests.org</a></li>
    </ul>
  </li>
  <li>datetime
    <ul>
      <li>Purpose: To get the current hour to determine if it's night.</li>
    </ul>
  </li>
  <li>smtplib
    <ul>
      <li>Purpose: To send an email notification using Gmail SMTP server.</li>
      <li><a href="https://docs.python.org/3/library/smtplib.html" target="_blank">smtplib — SMTP protocol client</a></li>
    </ul>
  </li>
  <li>time
    <ul>
      <li>Purpose: Adds a 60-second interval between checks to avoid too frequent requests and emails.</li>
    </ul>
  </li>  
</ol>
<h3>🌐 APIs Used:</h3>
<ol>
  <li>ISS Position API
    <ul>
      <li><a href="http://api.open-notify.org/iss-now.json" target="_blank">http://api.open-notify.org/iss-now.json</a></li>
      <li>Purpose: Returns the current location of the ISS as latitude and longitude.</li>
      <p>Sample Response:
        {<br>
          "iss_position": {<br>
            "latitude": "47.6062",<br>
            "longitude": "-122.3321"<br>
            },<br>
          "timestamp": 1596567890,<br>
          "message": "success"<br>
        }<br>
      </p>
  </li>
  <li>Sunrise-Sunset API
    <ul>
      <li><a href="https://api.sunrise-sunset.org/json" target="_blank">https://api.sunrise-sunset.org/json</a></li>
      <li>Returns the sunrise and sunset times for a given location.</li>
      <p>Sample Response:
        {<br>
          "results": {<br>
            "sunrise": "2025-07-23T00:44:32+00:00",<br>
            "sunset": "2025-07-23T13:15:32+00:00",<br>
            ...<br>
          },<br>
          "status": "OK"<br>
        }<br>
      </p>
  </li>
</ol>










