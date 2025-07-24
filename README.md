# 🌌 ISS Overhead Notifier
<h2>🔎 Description:</h2>
<p>This Python-based project notifies you via email when the International Space Station (ISS) is passing over your location at night. 
  It checks your geographical position against the current ISS coordinates and verifies if it's currently nighttime in your location. 
  If both conditions are satisfied, an email alert is triggered to tell you to look up and try spotting the ISS in the night sky!</p>
<h2>Modules and Libraries Used</h2>
<ol>
  <li><b>requests</b>
    <ul>
      <li><b>Purpose:</b> To send HTTP requests to public APIs (ISS position & sunrise/sunset info).</li>
      <li><a href="https://docs.python-requests.org" target="_blank">https://docs.python-requests.org</a></li>
    </ul>
  </li>
  <li><b>datetime</b>
    <ul>
      <li><b>Purpose:</b> To get the current hour to determine if it's night.</li>
    </ul>
  </li>
  <li><b>smtplib</b>
    <ul>
      <li><b>Purpose:</b> To send an email notification using Gmail SMTP server.</li>
      <li><a href="https://docs.python.org/3/library/smtplib.html" target="_blank">smtplib — SMTP protocol client</a></li>
    </ul>
  </li>
  <li><b>time</b>
    <ul>
      <li><b></b>Purpose:</b> Adds a 60-second interval between checks to avoid too frequent requests and emails.</li>
    </ul>
  </li>  
</ol>
<h3>🌐 APIs Used:</h3>
<ol>
  <li><b>ISS Position API</b>
    <ul>
      <li><a href="http://api.open-notify.org/iss-now.json" target="_blank">http://api.open-notify.org/iss-now.json</a></li>
      <li><b>Purpose:</b> Returns the current location of the ISS as latitude and longitude.</li><br>
      <p><b>Sample Response:</b><br><br>
        {<br>
          "iss_position": {<br>
            "latitude": "47.6062",<br>
            "longitude": "-122.3321"<br>
            },<br>
          "timestamp": 1596567890,<br>
          "message": "success"<br>
        }<br>
      </p>
    </ul>
  </li>
  <li><b>Sunrise-Sunset API</b>
    <ul>
      <li><a href="https://api.sunrise-sunset.org/json" target="_blank">https://api.sunrise-sunset.org/json</a></li>
      <li>Returns the sunrise and sunset times for a given location.</li><br>
      <p><b>Sample Response:</b><br><br>
        {<br>
          "results": {<br>
            "sunrise": "2025-07-23T00:44:32+00:00",<br>
            "sunset": "2025-07-23T13:15:32+00:00",<br>
            ...<br>
          },<br>
          "status": "OK"<br>
        }<br>
      </p>
    </ul>
  </li>
</ol>










