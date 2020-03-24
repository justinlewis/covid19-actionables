---
layout: page
title: Problem Solvers
permalink: /problem-solvers/
---



{% for solution in site.data.problem-solvers %}

  <div class="solution-panel">
    <h2 class="solution-header">
      <img src="../images/logos/{{solution.logo}}" alt="logo" height="50" width="50">
      {{solution.title}}
    </h2>
    <p class="solution-problem"><strong>Problem:</strong> {{solution.problem}}</p>
    <p class="solution-solution"><strong>Solution:</strong> {{solution.solution}}</p>
    <!-- <p class="solution-description"><strong>Description:</strong> {{solution.description}}</p> -->

    {% if solution.helpinfo %}
    <a href="{{solution.helpinfo}}" class="solution-help-info" target="_blank">Ask for their help</a>
    {% endif %}

    {% if solution.twitter %}
    <a href="{{solution.twitter}}" style="color:#1DA1F2;" class="fab fa-twitter solution-contact-icon" target="_blank"></a>
    {% endif %}

    {% if solution.facebook %}
    <a href="{{solution.facebook}}" style="color: #4267b2;" class="fab fa-facebook solution-contact-icon" target="_blank"></a>
    {% endif %}

    {% if solution.source %}
    <a href="{{solution.source}}" class="solution-source-button" target="_blank">Source</a>
    {% endif %}

  </div>

{% endfor %}
