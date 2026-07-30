---
layout: default
title: Journal
permalink: /journal/
---

<div class="journal-page">

  <!-- =====================================================
       HERO
  ====================================================== -->

  <section class="journal-hero">

    <div class="journal-hero__inner">

      <div class="journal-hero__eyebrow">
        ICECORE DYNASTY
      </div>

      <h1>Journal</h1>

      <p>
        League news, strategy, guides and stories from across IceCore Dynasty.
      </p>

    </div>

  </section>


  <!-- =====================================================
       CONTENT
  ====================================================== -->

  <section class="journal-content">

    <div class="journal-intro">

      <div class="section-heading">
        <h2>From IceCore</h2>
      </div>

      <p>
        Follow the league beyond the standings. Explore official announcements,
        General Manager guides, league philosophy, strategy and stories from
        across IceCore Dynasty.
      </p>

    </div>


    {% assign journal_posts = site.posts | sort: "date" | reverse %}


    {% if journal_posts.size > 0 %}


      <!-- =====================================================
           ALL STORIES
      ====================================================== -->

      <section class="journal-section">

        <div class="journal-section__heading">

          <h2>All Stories</h2>

          <span>
            {{ journal_posts.size }}
            {% if journal_posts.size == 1 %}
              article
            {% else %}
              articles
            {% endif %}
          </span>

        </div>


        <div class="journal-grid">

          {% for post in journal_posts %}

            <article
              class="journal-card"
              data-category="{% if post.categories %}{{ post.categories | join: ' ' | downcase }}{% endif %}"
            >

              <a
                class="journal-card__image"
                href="{{ post.url | relative_url }}"
                aria-label="Read {{ post.title | escape }}"
              >

                {% if post.image %}

                  <img
                    src="{{ post.image | relative_url }}"
                    alt="{{ post.title | escape }}"
                    loading="lazy"
                    decoding="async"
                  >

                {% elsif post.header.teaser %}

                  <img
                    src="{{ post.header.teaser | relative_url }}"
                    alt="{{ post.title | escape }}"
                    loading="lazy"
                    decoding="async"
                  >

                {% endif %}

              </a>


              <div class="journal-card__content">

                <div class="journal-card__meta">

                  <span>
                    {{ post.date | date: "%b %d, %Y" | upcase }}
                  </span>

                  {% if post.categories and post.categories.size > 0 %}

                    <span class="journal-card__dot">·</span>

                    <span>
                      {{ post.categories | first | upcase }}
                    </span>

                  {% endif %}

                </div>


                <h3 class="journal-card__title">

                  <a href="{{ post.url | relative_url }}">
                    {{ post.title }}
                  </a>

                </h3>


                {% if post.excerpt %}

                  <p class="journal-card__excerpt">
                    {{ post.excerpt | strip_html | strip_newlines }}
                  </p>

                {% endif %}


                <a
                  class="journal-card__read"
                  href="{{ post.url | relative_url }}"
                >
                  Read story
                  <span aria-hidden="true">→</span>
                </a>

              </div>

            </article>

          {% endfor %}

        </div>

      </section>


      <!-- =====================================================
           STORIES BY CATEGORY
      ====================================================== -->

      {% assign journal_categories = site.categories | sort %}


      {% if journal_categories.size > 0 %}

        <section class="journal-categories">

          <div class="journal-section__heading">

            <h2>Browse by Category</h2>

            <span>
              {{ journal_categories.size }} categories
            </span>

          </div>


          {% for category in journal_categories %}

            {% assign category_name = category[0] %}
            {% assign category_posts = category[1] | sort: "date" | reverse %}


            <section
              class="journal-category"
              id="{{ category_name | slugify }}"
            >

              <div class="journal-category__heading">

                <div>

                  <span class="journal-category__label">
                    CATEGORY
                  </span>

                  <h3>
                    {{ category_name }}
                  </h3>

                </div>


                <span class="journal-category__count">

                  {{ category_posts.size }}

                  {% if category_posts.size == 1 %}
                    story
                  {% else %}
                    stories
                  {% endif %}

                </span>

              </div>


              <div class="journal-category__list">

                {% for post in category_posts %}

                  <a
                    class="journal-category__item"
                    href="{{ post.url | relative_url }}"
                  >

                    <div class="journal-category__meta">

                      <span>
                        {{ post.date | date: "%b %d, %Y" | upcase }}
                      </span>

                    </div>


                    <div class="journal-category__title">
                      {{ post.title }}
                    </div>


                    <span
                      class="journal-category__arrow"
                      aria-hidden="true"
                    >
                      →
                    </span>

                  </a>

                {% endfor %}

              </div>

            </section>

          {% endfor %}

        </section>

      {% endif %}


    {% else %}


      <div class="journal-empty">

        <h2>No stories yet.</h2>

        <p>
          The IceCore Journal is being prepared for the inaugural season.
        </p>

      </div>


    {% endif %}

  </section>

</div>
