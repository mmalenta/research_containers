---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default 
---

**Welcome to the Research Containers repository!**

# Motivation

# Available resources
<table>
  <thead>
    <tr>
      <th>Technology</th>
      <th>Resources</th>
    </tr>
  </thead>
  <tbody>
  {% for tech in site.technologies %}
    <tr><td><a href="{{ tech.url | absolute_url}}">{{ tech.name }}</a></td>
    <td>
    
    {% assign resource_files = site.collections | where: "label", "resources" | first %}

    {% assign all_files=resource_files.docs | concat: resource_files.files%}

    {% assign resources = "" %}
    {% for file in all_files %}

      {% assign split_file=file.path | split: "/" %}
      {% assign down_name = tech.name | downcase %}
      {% assign split_size = split_file | size %}
      {% if split_file[1] == down_name and split_size > 3 %}

        {% assign resources = resources | append: " " | append: split_file[2] %}

      {% endif %}

    {% endfor %}

        {% assign resources = resources | split: " " | uniq %}
        {% assign resources_size = resources | size %}

        {% if resources_size > 0 %}
          <ul>
          {% for resource in resources %}
            <li><a href="resources/{{down_name}}/{{down_name}}_resources.html#{{resource}}">{{ resource | capitalize }}</a></li>
          {% endfor %}
          </ul>
        {% endif %}
        
        </td></tr>
  
  {% endfor %}
  </tbody>
</table>

# Contact
No single containerisation technology can solve all the problems.
As the number of problems is growing, the number of available solutions
is becoming greater as well.
We are therefore asking for your contributions to this repository!
We are looking for lessons, hacks, tools and code you think that could
be of use to the research community and you are willing to share.
## Join us!

# Contributors
