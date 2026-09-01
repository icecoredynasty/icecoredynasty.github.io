---
title: Teams
permalink: /teams/
layout: icecore-page
author_profile: false
description: "Meet the twenty IceCore Dynasty franchises, their identities, cities, histories and the General Managers building them for the long term."
---

<section class="teams-hero">
  <div class="teams-hero__inner">
    <div class="teams-hero__copy">
      <span class="teams-hero__eyebrow">OUR FRANCHISES</span>
      <h1>EVERY FRANCHISE<br>HAS A STORY<span>.</span></h1>
      <div class="teams-hero__line"></div>
      <p>Every club has an identity.<br>Every identity has a legacy to build.</p>
    </div>
  </div>
</section>

<section class="teams-directory">
  <div class="teams-directory__inner">
    {% include team-grid.html %}

    <div class="teams-filters">
      <label class="teams-filter">
        <span>League</span>
        <select id="league-filter">
          <option value="all" selected>All Leagues</option>
          <option value="1">League 1</option>
          <option value="2">League 2</option>
        </select>
      </label>

      <label class="teams-filter">
        <span>Division</span>
        <select id="division-filter">
          <option value="all" selected>All Divisions</option>
          {% assign all_active = site.teams | where: "status", "active" %}
          {% assign all_divisions = all_active | map: "division" | compact | uniq | sort_natural %}
          {% for division in all_divisions %}
            {% if division != "" %}
              <option value="{{ division | downcase | escape }}">{{ division }} Division</option>
            {% endif %}
          {% endfor %}
        </select>
      </label>
    </div>
  </div>
</section>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const leagueFilter = document.getElementById("league-filter");
  const divisionFilter = document.getElementById("division-filter");
  const cards = document.querySelectorAll(".team-card");

  function filterTeams() {
    const selectedLeague = leagueFilter.value;
    const selectedDivision = divisionFilter.value;

    cards.forEach(function (card) {
      const cardLeague = card.dataset.league || "";
      const cardDivision = card.dataset.division || "";

      const leagueMatch = selectedLeague === "all" || cardLeague === selectedLeague;
      const divisionMatch = selectedDivision === "all" || cardDivision === selectedDivision;

      card.style.display = leagueMatch && divisionMatch ? "" : "none";
    });
  }

  leagueFilter.addEventListener("change", filterTeams);
  divisionFilter.addEventListener("change", filterTeams);
  filterTeams();
});
</script>
