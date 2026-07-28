---
layout: default
title: Journal
permalink: /journal/
---

<div class="ic-journal">

  <!-- HERO -->
  <section class="ic-journal-hero">

    <div class="ic-journal-hero__image">
      <img
        src="{{ '/assets/images/heroes/journal-hero.jpg' | relative_url }}"
        alt="IceCore Dynasty Journal"
      >
    </div>

    <div class="ic-journal-hero__content">
      <span class="ic-journal-eyebrow">
        ICECORE DYNASTY · JOURNAL
      </span>

      <h1>Stories behind the standings.</h1>

      <p>
        League news, franchise stories, guides, draft coverage
        and the decisions shaping IceCore Dynasty.
      </p>
    </div>

  </section>


  <!-- STORIES -->
  <section class="ic-journal-section">

    <header class="ic-journal-heading">
      <span>JOURNAL</span>
      <h2>Latest stories.</h2>
    </header>


    <!-- FILTERS -->
    <div class="ic-journal-filters">

      <label>
        <span>League</span>

        <select id="journalLeague">
          <option value="all">All Leagues</option>
          <option value="league-1">League 1</option>
          <!--
          <option value="league-2">League 2</option>
          -->
        </select>
      </label>


      <label>
        <span>Category</span>

        <select id="journalCategory">
          <option value="all">All Categories</option>
          <option value="league">League News</option>
          <option value="franchise">Franchises</option>
          <option value="draft">Draft</option>
          <option value="guide">Guides</option>
          <option value="analysis">Analysis</option>
          <option value="history">History</option>
        </select>
      </label>


      <label>
        <span>Season</span>

        <select id="journalSeason">
          <option value="all">All Seasons</option>
          <option value="2026-27">2026–27</option>
        </select>
      </label>

    </div>


    <!-- ARTICLE GRID -->
    <div class="ic-journal-grid" id="journalArchive">


      <!-- FEATURED / NEWEST ARTICLE -->
      <article
        class="ic-journal-card ic-journal-card--lead"
        data-league="league-1"
        data-category="league"
        data-season="2026-27"
      >

        <a
          class="ic-journal-card__image"
          href="{{ '/journal/inaugural-season/' | relative_url }}"
        >
          <img
            src="{{ '/assets/images/journal/inaugural-season.jpg' | relative_url }}"
            alt=""
          >
        </a>

        <div class="ic-journal-card__content">

          <div class="ic-journal-card__meta">
            <span>League 1</span>
            <span>League News</span>
            <time>2026</time>
          </div>

          <h3>
            <a href="{{ '/journal/inaugural-season/' | relative_url }}">
              A new dynasty begins.
            </a>
          </h3>

          <p>
            Twenty franchises. Permanent identities. One shared history
            waiting to be written.
          </p>

          <a
            class="ic-journal-card__read"
            href="{{ '/journal/inaugural-season/' | relative_url }}"
          >
            Read story →
          </a>

        </div>

      </article>


      <!-- GM GUIDE -->
      <article
        class="ic-journal-card"
        data-league="all"
        data-category="guide"
        data-season="2026-27"
      >

        <a
          class="ic-journal-card__image"
          href="{{ '/journal/gm-guide/' | relative_url }}"
        >
          <img
            src="{{ '/assets/images/journal/gm-guide.jpg' | relative_url }}"
            alt=""
          >
        </a>

        <div class="ic-journal-card__content">

          <div class="ic-journal-card__meta">
            <span>All Leagues</span>
            <span>Guide</span>
            <time>2026</time>
          </div>

          <h3>
            <a href="{{ '/journal/gm-guide/' | relative_url }}">
              The General Manager's Guide to IceCore.
            </a>
          </h3>

          <p>
            The essentials of salaries, keepers, prospects,
            drafts and long-term franchise management.
          </p>

          <a
            class="ic-journal-card__read"
            href="{{ '/journal/gm-guide/' | relative_url }}"
          >
            Read story →
          </a>

        </div>

      </article>


      <!-- ENTRY DRAFT -->
      <article
        class="ic-journal-card"
        data-league="all"
        data-category="draft"
        data-season="2026-27"
      >

        <a
          class="ic-journal-card__image"
          href="{{ '/journal/entry-draft-guide/' | relative_url }}"
        >
          <img
            src="{{ '/assets/images/journal/entry-draft-guide.jpg' | relative_url }}"
            alt=""
          >
        </a>

        <div class="ic-journal-card__content">

          <div class="ic-journal-card__meta">
            <span>All Leagues</span>
            <span>Draft</span>
            <time>2026</time>
          </div>

          <h3>
            <a href="{{ '/journal/entry-draft-guide/' | relative_url }}">
              Inside the IceCore Entry Draft.
            </a>
          </h3>

          <p>
            One rookie per franchise, reverse standings and no lottery:
            the system behind IceCore's annual rookie class.
          </p>

          <a
            class="ic-journal-card__read"
            href="{{ '/journal/entry-draft-guide/' | relative_url }}"
          >
            Read story →
          </a>

        </div>

      </article>

    </div>


    <div class="ic-journal-empty" id="journalEmpty">
      No stories match these filters.
    </div>

  </section>


  <!-- SECTIONS -->
  <section class="ic-journal-section ic-journal-sections">

    <header class="ic-journal-heading">
      <span>SECTIONS</span>
      <h2>Inside the Journal.</h2>
    </header>


    <div class="ic-journal-categories">

      <article>
        <span>01</span>
        <h3>League News</h3>
        <p>
          Announcements, milestones, expansion and major developments
          across IceCore.
        </p>
      </article>

      <article>
        <span>02</span>
        <h3>Franchises</h3>
        <p>
          Team stories, rebuilds, rivalries and the people behind
          IceCore's permanent clubs.
        </p>
      </article>

      <article>
        <span>03</span>
        <h3>Draft</h3>
        <p>
          Rookie classes, Salary Cap Drafts and the decisions shaping
          the next generation.
        </p>
      </article>

      <article>
        <span>04</span>
        <h3>Guides</h3>
        <p>
          Clear explanations of IceCore systems for new and returning
          General Managers.
        </p>
      </article>

      <article>
        <span>05</span>
        <h3>Analysis</h3>
        <p>
          Salary value, roster construction, league trends and strategy.
        </p>
      </article>

      <article>
        <span>06</span>
        <h3>History</h3>
        <p>
          Championships, records and defining moments from every
          IceCore season.
        </p>
      </article>

    </div>

  </section>


  <!-- CLOSING -->
  <section class="ic-journal-closing">

    <span>THE ARCHIVE STARTS HERE</span>

    <h2>
      Today is news.<br>
      Tomorrow is history.
    </h2>

    <p>
      Every draft, championship, rebuild and era adds another chapter
      to the IceCore archive.
    </p>

    <strong>Season One · 2026–27</strong>

  </section>

</div>


<script>
document.addEventListener("DOMContentLoaded", function () {

  const leagueFilter = document.getElementById("journalLeague");
  const categoryFilter = document.getElementById("journalCategory");
  const seasonFilter = document.getElementById("journalSeason");

  const articles = document.querySelectorAll(".ic-journal-card");
  const emptyState = document.getElementById("journalEmpty");

  function filterJournal() {

    const league = leagueFilter.value;
    const category = categoryFilter.value;
    const season = seasonFilter.value;

    let visible = 0;

    articles.forEach(function (article) {

      const leagueMatch =
        league === "all" ||
        article.dataset.league === "all" ||
        article.dataset.league === league;

      const categoryMatch =
        category === "all" ||
        article.dataset.category === category;

      const seasonMatch =
        season === "all" ||
        article.dataset.season === season;

      const show =
        leagueMatch &&
        categoryMatch &&
        seasonMatch;

      article.hidden = !show;

      if (show) visible++;

    });

    emptyState.style.display =
      visible === 0 ? "block" : "none";
  }

  leagueFilter.addEventListener("change", filterJournal);
  categoryFilter.addEventListener("change", filterJournal);
  seasonFilter.addEventListener("change", filterJournal);

  filterJournal();

});
</script>
