---
layout: single
title: "Misc"
permalink: /misc/
author_profile: true
---

<link
  rel="stylesheet"
  href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
/>

<script
  src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js">
</script>

## National Parks

I have visited the following U.S. national parks.

<div id="parks-map" style="height: 500px; width: 100%; border-radius: 8px; margin: 1.5rem 0;"></div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    var map = L.map("parks-map").setView([39.5, -98.35], 4);

    L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
      maxZoom: 18,
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);

    var parks = [
      { name: "Arches National Park", state: "UT", lat: 38.7331, lng: -109.5925, visited: "2024" },
      { name: "Badlands National Park", state: "SD", lat: 43.8554, lng: -102.3397, visited: "2026" },
      { name: "Theodore Roosevelt National Park", state: "ND", lat: 46.9790, lng: -103.5387, visited: "2026" },
      { name: "Bryce Canyon National Park", state: "UT", lat: 37.5930, lng: -112.1871, visited: "2024" },
      { name: "Capitol Reef National Park", state: "UT", lat: 38.0877, lng: -111.1355, visited: "2024" },
      { name: "Channel Islands National Park", state: "CA", lat: 34.0069, lng: -119.7785, visited: "2026" },
      { name: "Congaree National Park", state: "SC", lat: 33.7919, lng: -80.7487, visited: "2025" },
      { name: "Death Valley National Park", state: "CA / NV", lat: 36.5054, lng: -117.0794, visited: "2025" },
      { name: "Grand Canyon National Park", state: "AZ", lat: 36.1069, lng: -112.1129, visited: "2012" },
      { name: "Great Sand Dunes National Park", state: "CO", lat: 37.7329, lng: -105.5126, visited: "2024" },
      { name: "Hawaiʻi Volcanoes National Park", state: "HI", lat: 19.4194, lng: -155.2885, visited: "2014" },
      { name: "Indiana Dunes National Park", state: "IN", lat: 41.6533, lng: -87.0524, visited: "2025" },
      { name: "Joshua Tree National Park", state: "CA", lat: 33.8734, lng: -115.9010, visited: "2024" },
      { name: "Kings Canyon National Park", state: "CA", lat: 36.8879, lng: -118.5551, visited: "2025" },
      { name: "Mammoth Cave National Park", state: "KY", lat: 37.1862, lng: -86.1005, visited: "2025" },
      { name: "New River Gorge National Park and Preserve", state: "WV", lat: 37.9263, lng: -81.1547, visited: "2025" },
      { name: "Sequoia National Park", state: "CA", lat: 36.4864, lng: -118.5658, visited: "2025" },
      { name: "Shenandoah National Park", state: "VA", lat: 38.2928, lng: -78.6796, visited: "2025" },
      { name: "Wind Cave National Park", state: "SD", lat: 43.5724, lng: -103.4416, visited: "2026" },
      { name: "Yellowstone National Park", state: "WY / MT / ID", lat: 44.4280, lng: -110.5885, visited: "2012" },
      { name: "Yosemite National Park", state: "CA", lat: 37.8651, lng: -119.5383, visited: "2012" },
      { name: "Zion National Park", state: "UT", lat: 37.2982, lng: -113.0263, visited: "2024" }
    ];

    parks.forEach(function (park) {
      L.marker([park.lat, park.lng])
        .addTo(map)
        .bindPopup(
          "<strong>" + park.name + "</strong><br>" +
          park.state + "<br>" +
          "Visited: " + park.visited
        );
    });
  });
</script>



<!-- <div style="text-align: center;">
  <img src="/images/first_university.jpg" alt="First day in university" style="width:500px; border-radius:8px;">
  <p style="font-size: 0.9em; color: #555;">
    First day in university, summer 2019. And I was in the
    <a href="https://news.pku.edu.cn/xwzh/0c3eada2ae214f7797e937dded50ec8d.htm" target="_blank">news</a>!
  </p>
</div>

<div style="text-align: center; margin-top: 30px;">
  <img src="/images/graduation.jpg" alt="Last day in university" style="width:500px; border-radius:8px;">
  <p style="font-size: 0.9em; color: #555;">Last day in university, summer 2023</p>
</div> -->
