---
title: "Tools & Resources"
permalink: /tools/
author_profile: true
---

A collection of tools, links, and resources I use or find useful or interesting!

## General ressources

- [PlanetTerre](https://planet-terre.ens-lyon.fr/) — A wide range of articles on geological topics, for multiple levels (in French)
- [PlanetVie](https://planet-vie.ens.fr/) — Same concept, for biology (in French)
  

## Software
- [gospl](https://github.com/Geodels/gospl) — Landscape Evolution Model, developed by Tristan Salles
- [IPSL-CM5A2](https://cmc.ipsl.fr/models/ipsl-climate-models/ipsl-cm5a2/) — Coupled climate model


## Map of Talks & Conferences

<div id="conf-map" style="height: 400px; border-radius: 10px; margin: 1.5em 0;"></div>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.9.4/leaflet.min.css" />

<script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.9.4/leaflet.min.js"></script>

<script>

  var map = L.map('conf-map').setView([35, 10], 2);

  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {

    attribution: '&copy; OpenStreetMap contributors'

  }).addTo(map);

  function coloredIcon(color) {

    return L.divIcon({

      className: '',

      html: '<div style="background:' + color + '; width: 14px; height: 14px; border-radius: 50%; border: 2px solid white; box-shadow: 0 0 3px rgba(0,0,0,0.5);"></div>',

      iconSize: [14, 14],

      iconAnchor: [7, 7]

    });

  }

  var events = [

    {name: "RST 2025", city: "Montpellier, France", lat: 43.6108, lng: 3.8767, type: "conference"},

    {name: "EGU 2026", city: "Vienna, Austria", lat: 48.2082, lng: 16.3738, type: "conference"},

    {name: "ESHE 2025", city: "Paris, France", lat: 48.8566, lng: 2.3522, type: "conference"},

    {name: "Seminar — ISTerre/Palevoprim", city: "Poitiers, France", lat: 46.5802, lng: 0.3404, type: "conference"},

    {name: "PhD presentation — Centre Géologique de l'Oisans", city: "Bourg-d'Oisans, France", lat: 45.0587, lng: 6.0303, type: "outreach"},

    {name: "Teacher training — Erosion & biodiversity", city: "Grenoble, France", lat: 45.1885, lng: 5.7245, type: "outreach"}

  ];

  var colors = { conference: "#f39c12", outreach: "#27ae60" };

  events.forEach(function(e) {

    L.marker([e.lat, e.lng], {icon: coloredIcon(colors[e.type])})

      .addTo(map)

      .bindPopup("<strong>" + e.name + "</strong><br/>" + e.city);

  });

</script>

**Legend:** 🟠 Conferences · 🟢 Talks & Outreach 
