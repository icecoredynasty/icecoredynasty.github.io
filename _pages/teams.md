---
title: Teams
permalink: /teams/
layout: icecore-page
author_profile: false
---

<section class="teams-hero">

  <div class="teams-hero__inner">

    <div class="teams-hero__copy">

      <span class="teams-hero__eyebrow">
        OUR FRANCHISES
      </span>

      <h1>
        EVERY FRANCHISE<br>
        HAS A STORY<span>.</span>
      </h1>

      <div class="teams-hero__line"></div>

      <p>
        Every club has an identity.<br>
        Every identity has a legacy to build.
      </p>

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
  <option value="all">All Leagues</option>
  <option value="1" selected>League I</option>
</select>
        </label>

        <label class="teams-filter">
          <span>Conference</span>

<select id="conference-filter">
  <option value="all">All Conferences</option>
  <option value="east">Eastern Conference</option>
  <option value="west">Western Conference</option>
</select>
        </label>

      </div>
      
  </div>

</section>

<script>
document.addEventListener("DOMContentLoaded", function () {

  const leagueFilter = document.getElementById("league-filter");
  const conferenceFilter = document.getElementById("conference-filter");
  const cards = document.querySelectorAll(".team-card");

  function filterTeams() {

    const selectedLeague = leagueFilter.value;
    const selectedConference = conferenceFilter.value;

    cards.forEach(function(card) {

      const cardLeague = card.dataset.league;
      const cardConference = card.dataset.conference;

      const leagueMatch =
        selectedLeague === "all" ||
        cardLeague === selectedLeague;

      const conferenceMatch =
        selectedConference === "all" ||
        cardConference === selectedConference;

      if (leagueMatch && conferenceMatch) {
        card.style.display = "";
      } else {
        card.style.display = "none";
      }

    });

  }

  leagueFilter.addEventListener("change", filterTeams);
  conferenceFilter.addEventListener("change", filterTeams);

  filterTeams();

});
</script>

