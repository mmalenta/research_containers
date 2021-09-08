---
layout : default
name: "docker"
title: "Docker resources"
permalink: /resources/docker/docker_resources
---

# Docker resources

{% assign resource_files = site.collections | where: "label", "resources" | first %}

<h2 id="lessons">Lessons</h2>
  <table>
    <thead>
      <tr>
        <th>Lesson #</th>
        <th>Lesson title</th>
        <th>Duration</th>
      </tr>
    </thead>
    <tbody>
      {% for file in resource_files.docs %}

        {% assign split_file=file.path | split: "/" %}
        {% if split_file[1] == page.name and split_file[2] == "lessons" %}

          <tr>
            {% if file.lesson_section %}
              <td class="sublesson">{{file.lesson_number}}</td>
            {% else %}
              <td>{{file.lesson_number}}</td>
            {% endif %}
            <td><a href="{{file.url | absolute_url}}">{{file.lesson_title}}</a></td>
            <td>{{file.lesson_duration}}</td>
          </tr>

        {% endif %}

      {% endfor %}
    
    </tbody>
</table>

<h2 id="dockerfiles">Dockerfiles</h2>

{% for file in resource_files.files %}

  {% assign split_file=file.path | split: "/" %}
  {% if split_file[1] == page.name %}
  <div class="code">
    <a href="{{file.path | replace: '_resources/docker/', ''}}">{{split_file[3]}}</a>
    <pre class="snippet"><code>{% include_relative {{file.path | replace: "_resources/docker/", ""}} %}</code></pre>
  </div>

  {% endif %}
{% endfor %}
