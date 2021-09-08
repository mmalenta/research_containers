---
layout : default
name: "docker"
title: "Docker resources"
permalink: /resources/docker/docker_resources
---

# Docker resources

<h2 id="lessons">Lessons</h2>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Risus commodo viverra maecenas accumsan lacus vel facilisis volutpat est. Arcu cursus euismod quis viverra nibh cras pulvinar mattis nunc. Interdum posuere lorem ipsum dolor sit amet. Mattis ullamcorper velit sed ullamcorper morbi tincidunt ornare massa eget. Bibendum arcu vitae elementum curabitur vitae nunc. Lectus nulla at volutpat diam ut venenatis. Tincidunt augue interdum velit euismod in pellentesque. Et tortor at risus viverra adipiscing at. Lacus sed turpis tincidunt id.

Blandit massa enim nec dui nunc. Risus in hendrerit gravida rutrum quisque. Aliquet bibendum enim facilisis gravida. Sed viverra ipsum nunc aliquet. Lectus nulla at volutpat diam. Convallis posuere morbi leo urna. Pellentesque pulvinar pellentesque habitant morbi tristique. Ut lectus arcu bibendum at varius vel pharetra. Proin sagittis nisl rhoncus mattis rhoncus urna neque. Eget duis at tellus at urna condimentum mattis pellentesque. Iaculis eu non diam phasellus vestibulum lorem sed. Tincidunt id aliquet risus feugiat in ante metus dictum at. Elementum eu facilisis sed odio morbi. Ligula ullamcorper malesuada proin libero nunc consequat interdum varius sit.

<h2 id="dockerfiles">Dockerfiles</h2>

{% assign resource_files = site.collections | where: "label", "resources" | first %}
{% for file in resource_files.files %}

  {% assign split_file=file.path | split: "/" %}
  {% if split_file[1] == page.name %}
  <div class="code">
    <pre class="snippet"><code>{% include_relative {{file.path | replace: "_resources/docker/", ""}} %}</code></pre>
  </div>

  {% endif %}
{% endfor %}

Morbi blandit cursus risus at. Enim neque volutpat ac tincidunt vitae semper quis lectus. Netus et malesuada fames ac turpis egestas sed. Turpis massa tincidunt dui ut. Nam aliquam sem et tortor consequat id porta. Egestas sed tempus urna et pharetra pharetra massa massa. Sed augue lacus viverra vitae congue eu consequat ac. Egestas erat imperdiet sed euismod nisi porta lorem. Nulla malesuada pellentesque elit eget gravida cum. Facilisis leo vel fringilla est. Mauris augue neque gravida in fermentum et. Suscipit adipiscing bibendum est ultricies integer quis. Scelerisque purus semper eget duis at. Tellus integer feugiat scelerisque varius morbi enim. Euismod nisi porta lorem mollis aliquam ut. Est sit amet facilisis magna etiam tempor orci. Leo a diam sollicitudin tempor. Senectus et netus et malesuada fames ac turpis egestas.
Ut etiam sit amet nisl. Pellentesque habitant morbi tristique senectus et netus et. Eros in cursus turpis massa. Tincidunt praesent semper feugiat nibh. Vulputate dignissim suspendisse in est ante in nibh. Adipiscing diam donec adipiscing tristique risus nec. Quisque egestas diam in arcu cursus. Pretium aenean pharetra magna ac placerat vestibulum lectus. Elit at imperdiet dui accumsan sit amet nulla. Mauris a diam maecenas sed enim ut sem viverra. Massa sed elementum tempus egestas sed sed. Lectus nulla at volutpat diam ut venenatis tellus in metus. Tristique nulla aliquet enim tortor at auctor urna. Lectus mauris ultrices eros in cursus. Semper auctor neque vitae tempus quam pellentesque. Euismod elementum nisi quis eleifend quam adipiscing vitae proin sagittis. Pulvinar mattis nunc sed blandit libero volutpat sed cras. Aliquam sem et tortor consequat id porta nibh venenatis cras. At tellus at urna condimentum mattis pellentesque id 
