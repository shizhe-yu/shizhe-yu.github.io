---
layout: single
title: "Misc"
permalink: /personal/
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

I have visited several U.S. national parks. This map records the parks I have been to.

<div id="parks-map" style="height: 500px; width: 100%; border-radius: 8px; margin: 1.5rem 0;"></div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    var map = L.map("parks-map").setView([39.5, -98.35], 4);

    L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
      maxZoom: 18,
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);

    var parks = [
      {
        name: "Yellowstone National Park",
        state: "WY / MT / ID",
        lat: 44.4280,
        lng: -110.5885,
        visited: "2023"
      },
      {
        name: "Grand Teton National Park",
        state: "WY",
        lat: 43.7904,
        lng: -110.6818,
        visited: "2023"
      },
      {
        name: "Yosemite National Park",
        state: "CA",
        lat: 37.8651,
        lng: -119.5383,
        visited: "2024"
      }
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
