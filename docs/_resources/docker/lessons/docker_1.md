---
layout : lesson
technology: "Docker"
lesson_number: "1.0"
lesson_title: "Introduction"
lesson_duration: "0h15m"
lesson_subsection: false
permalink: /resources/docker/lessons/docker_10
---
{% assign lower_tech = page.technology | downcase %}

Since its initial release in 2013, Docker has been widely adopted in many areas of research and the ‘industry‘. It is used to provide access to e-commerce and streaming services, machine learning platforms and, more generally, as a tool for distributing consistent software environments. Currently it is one of many existing container technologies that researchers can choose from, such as Singularity and Podman. Some solutions offer better support for High Performance Computing, when others provide a low-level control of the environment. It is therefore possible that after taking this course and familiarising yourself with other containerisation solutions, you might decide that Docker is not be the ideal fit for your requirements. Despite the strong competition and some notable shortcomings, Docker is still a popular choice and is often seen as a standard for containers.

{% assign main_lesson = page.lesson_number | split: "." | first %}

{% assign resource_files = site.collections | where: "label", "resources" | first %}

{% for file in resource_files.docs %}


  {% assign split_file=file.path | split: "/" %}
  {% if split_file[1] == lower_tech and split_file[2] == "lessons" %}

    {% unless page.lesson_number == file.lesson_number %}
      
      {% assign sub_parent = file.lesson_number | split: "." | first %}
      {% if sub_parent == main_lesson %}  
## {{file.technology}} {{file.lesson_number}}: {{file.lesson_title}}
{{ file.content }}
      {% endif %}
    {% endunless %}

  {% endif %}
{% endfor %}
