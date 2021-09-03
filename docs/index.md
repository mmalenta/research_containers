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
{% for file in site.pages %}
  {% if file.dir == "/technologies/" %}
    <tr><td><a href="{{ file.path | replace: '.md', '.html' }}">{{ file.name | replace: ".md", "" | capitalize }}</a></td>
    <td></td></tr>
  
  {% endif %}
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
