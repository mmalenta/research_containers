---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default 
---

**Welcome to the Research Containers repository!**

# Motivation

# Available resources

<!-- Markdown can get messy with list in a table
  Go with a raw HTML -->
<table>
  <thead>
    <tr>
      <th>Technology</th>
      <th>Resources</th>
    </tr>
  </thead>
  <tbody id="technologies">
    
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

<script>

  // This solution is taken from TimE's answer to
  // https://stackoverflow.com/questions/39048654/how-to-enable-directory-indexing-on-github-pages

  (async () => {
    const response = await fetch("https://api.github.com/repos/mmalenta/research_containers/contents/docs/technologies");
    const data = await response.json();
    let htmlString = "";
    for (let file of data) {
      htmlString += "<tr><td>"
      htmlString +=`<a href="${file.path.replace("docs/", "").replace(".md", ".html")}">${file.name.replace(".md", "")}</a></li>`;
      htmlString += "</td><td></td></tr>";
    }
    document.getElementById("technologies").innerHTML = htmlString;
  })()
</script>