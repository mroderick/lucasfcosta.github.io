---
layout: page
title: Talks
permalink: /talks/
---

<div class="home">
  <ul class="post-list">
    {% assign sortedTalks = (site.talks | sort: 'date') | reverse %}
    {% for talk in sortedTalks | sort: 'date' %}
      <li>

        <div class="post-meta">{{ talk.event }} • {{ talk.date | date: "%b %-d, %Y" }}</div>
        <h2>
          <a class="post-link" href="{{ talk.url | prepend: site.baseurl }}">{{ talk.title }}</a>
        </h2>

      </li>
    {% endfor %}
  </ul>
</div>
