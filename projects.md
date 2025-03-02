---
layout: page
permalink: /projects/
title: Projects
class: projects
---

{:.hidden}
# Projects

{:.lead}
Beyond my research, I have led or contributed to many projects with impactful deliverables. I feel deeply honored to collaborate with people from interdisciplinary backgrounds, which allows me to see the world from diverse perspectives. Feel free to reach out and I’d be delighted to share fascinating experiences and insights with you!

<div class="grid">
  {% for project in site.data.projects %}
    {% include project.html project=project %}
  {% endfor %}
</div>
