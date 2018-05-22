---
layout: default
title: Lesson Calendar
navigation: 6
---

<h1>Physics Lessons and key dates</h1>
  <div id="calendar-goes-here"></div>
  <small>Add events to this <a href="https://docs.google.com/a/github.com/spreadsheet/ccc?key=1jp84tZWSheS3E8g_AQaBJ8gYvBk-RXOVIiT26vOarOA#gid=0&output=json" target="_blank">spreadsheet</a>. Visit the GitHub <a href="http://www.github.com/jlord/sheetsee-calendar">repository</a>.</small>

  </body>
    <script type="text/javascript">
    document.addEventListener('DOMContentLoaded', function() {
      var URL = "1jp84tZWSheS3E8g_AQaBJ8gYvBk-RXOVIiT26vOarOA"
      Tabletop.init( { key: URL, callback: generateCalendar, simpleSheet: true } )
    })
  </script>
