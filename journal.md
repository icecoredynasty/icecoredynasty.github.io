---
layout: default
title: Journal
permalink: /journal/
---

<div class="ic-journal">


  <!-- =====================================================
       ARTICLES
       ===================================================== -->

  <section class="ic-journal-section">

    <header class="ic-journal-heading">

      <span>FROM THE LEAGUE</span>

      <h2>
        Stories from the league.
      </h2>

    </header>


    {% assign journal_posts = site.posts | sort: "date" | reverse %}


    {% if journal_posts.size > 0 %}

      <div class="ic-journal-grid">

        {% for post in journal_posts %}

          <article
            class="ic-journal-card{% if forloop.first %} ic-journal-card--lead{% endif %}"
          >

            {% if post.image %}

              <a
                class="ic-journal-card__image"
                href="{{ post.url | relative_url }}"
                aria-label="Read {{ post.title | escape }}"
              >

                <img
                  src="{{ post.image | relative_url }}"
                  alt="{{ post.title | escape }}"
                  loading="lazy"
                  decoding="async"
                >

              </a>

            {% elsif post.header.teaser %}

              <a
                class="ic-journal-card__image"
                href="{{ post.url | relative_url }}"
                aria-label="Read {{ post.title | escape }}"
              >

                <img
                  src="{{ post.header.teaser | relative_url }}"
                  alt="{{ post.title | escape }}"
                  loading="lazy"
                  decoding="async"
                >

              </a>

            {% endif %}


            <div class="ic-journal-card__content">

              <div class="ic-journal-card__meta">

                <span>
                  {{ post.date | date: "%b %d, %Y" }}
                </span>

                {% if post.categories and post.categories.size > 0 %}

                  <span>
                    {{ post.categories | first }}
                  </span>

                {% endif %}

              </div>


              <h3>

                <a href="{{ post.url | relative_url }}">
                  {{ post.title }}
                </a>

              </h3>


              {% if post.excerpt %}

                <p>
                  {{ post.excerpt | strip_html | strip_newlines }}
                </p>

              {% endif %}


              <a
                class="ic-journal-card__read"
                href="{{ post.url | relative_url }}"
              >
                Read story →
              </a>

            </div>

          </article>

        {% endfor %}

      </div>


      <div class="ic-journal-empty">
        No stories match the selected filters.
      </div>


    {% else %}


      <div
        class="ic-journal-empty"
        style="display:block;"
      >

        No stories yet.

      </div>


    {% endif %}

  </section>


  <!-- =====================================================
       JOURNAL SECTIONS
       ===================================================== -->

  <section class="ic-journal-section ic-journal-sections">

    <header class="ic-journal-heading">

      <span>EXPLORE</span>

      <h2>
        Inside IceCore.
      </h2>

    </header>


    <div class="ic-journal-categories">


      <article>

        <span>01</span>

        <h3>League</h3>

        <p>
          The format, philosophy and systems that define
          IceCore Dynasty.
        </p>

      </article>


      <article>

        <span>02</span>

        <h3>Strategy</h3>

        <p>
          Roster construction, salary management,
          trades, waivers and long-term decisions.
        </p>

      </article>


      <article>

        <span>03</span>

        <h3>Draft</h3>

        <p>
          Entry Draft strategy, prospects,
          scouting and the live player market.
        </p>

      </article>


      <article>

        <span>04</span>

        <h3>Scoring</h3>

        <p>
          The Fibonacci scoring system,
          player value and how IceCore rewards performance.
        </p>

      </article>


      <article>

        <span>05</span>

        <h3>Franchises</h3>

        <p>
          Team stories, General Managers,
          rivalries and the identities behind the league.
        </p>

      </article>


      <article>

        <span>06</span>

        <h3>History</h3>

        <p>
          Championships, records, awards
          and the moments that become part of IceCore.
        </p>

      </article>


    </div>

  </section>


  <!-- =====================================================
       CLOSING
       ===================================================== -->

  <section class="ic-journal-closing">

    <span>THE STORY CONTINUES</span>

    <h2>
      Every season<br>
      leaves something behind.
    </h2>

    <p>
      Draft picks become stars. Trades reshape franchises.
      Prospects arrive. Contenders fall. Champions emerge.
      The Journal records the decisions and moments that build
      IceCore history.
    </p>

    <strong>
      Twenty franchises. One shared history.
    </strong>

  </section>


</div>

/* =========================================================
   JOURNAL PAGE
   ========================================================= */

.layout--default .initial-content {
  padding-top: 0;
}

.ic-journal {
  margin-top: 2rem;
}
