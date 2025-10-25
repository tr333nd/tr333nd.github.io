<html><body>

<head>
    <link rel="stylesheet" href="stylesheet.css">
    <h1>This is Heading #1</h1>
    <p>This is an example of a paraghraph...</p>
</head>

async function fetchCalendar() {
  const response = await fetch('https://forex-factory-scraper1.p.rapidapi.com/calendar', {
    method: 'GET',
    headers: {
      'X-RapidAPI-Key': '535f2f6bbcmsh53c40dc21ddecb7p1ed1d9jsnddf0429dae8b',
      'X-RapidAPI-Host': 'forex-factory-scraper1.p.rapidapi.com'
    }
  });
  const data = await response.json(); // Array of events
  return data;
}

<table id="calendar-table">
  <thead><tr><th>Time</th><th>Event</th><th>Impact</th><th>Forecast</th></tr></thead>
  <tbody id="events-body"></tbody>
</table>
<script>
  // After filtering, loop through filteredData and append rows
  filteredData.forEach(event => {
    document.getElementById('events-body').innerHTML += 
      `<tr><td>${event.time}</td><td>${event.title}</td><td>${event.impact}</td><td>${event.forecast}</td></tr>`;
  });
</script>

</body></html>
