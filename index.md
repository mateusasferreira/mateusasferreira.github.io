---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default

title: Mateus Ferreira
description: >
    My beautiful resume
technologies:
  title: Technologies
  sections:
    - title: That I've been working with on a daily basis
      entries:
        - name: Node.js
          src_path: /assets/img/nodejs-original.svg
        - name: Python
          src_path: /assets/img/python-original.svg
    - title: That I use sometimes or have used for a while
      entries:
        - name: React
          src_path: /assets/img/react-original.svg
        - name: Angular
          src_path: /assets/img/angularjs-original.svg
experience:
  title: Professional Experience
  entries:
    - name: Maistodos
      position: Software Engineer
      period: Jun/2022 - ongoing
      description: >
        Aliqua consequat est sunt irure. Occaecat et minim sunt consectetur voluptate minim cillum culpa. Duis proident officia labore aliquip ea proident quis magna eiusmod magna. Anim est cillum tempor nulla culpa anim.
    - name: Anbetec
      position: Software Engineer
      period: Feb/2022 - May/2022
      description: >
        Aliqua consequat est sunt irure. Occaecat et minim sunt consectetur voluptate minim cillum culpa. Duis proident officia labore aliquip ea proident quis magna eiusmod magna. Anim est cillum tempor nulla culpa anim.
    - name: Haittane
      position: Software Engineer
      period: Aug/2021 - Feb/2022
      description: >
        Aliqua consequat est sunt irure. Occaecat et minim sunt consectetur voluptate minim cillum culpa. Duis proident officia labore aliquip ea proident quis magna eiusmod magna. Anim est cillum tempor nulla culpa anim.
education:
  title: Education
  entries:
    - institution: Faculdade Impacta
      period: Feb/2021 - Dec/2023
      name: Software Analysis and Development
      type: Technologist Degree
extras:
  - title: Languages
    entries:
      - Portuguese (Native)
      - English (Fluent)
      - Spanish (Advanced)
  - title: Soft Skilss
    entries:
      - Communication
      - Team Playing
      - Curiosity
      - Fast Learning
  - title: Hobbies
    entries:
      - Cooking
      - Music
      - Football



---

# {{ page.title }}

### {{page.description}}

<div style="display: flex; gap: 5px">
 <a href="{{site.linkedin}}" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
<a href = "mailto:{{site.email}}"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
</div>


<div class="section">
  <h2>{{ page.technologies.title }}</h2>
  {% for section in page.technologies.sections %}
    <h3>{{section.title}}</h3>
    {% for item in section.entries %}
      <img src="{{item.src_path}}" class="icon">
    {% endfor %}
  {% endfor %}
</div>

<div class="section">
  <h2> {{ page.experience.title }} </h2>
  {% for item in page.experience.entries %}
    <h3> {{item.name}} </h3>
    <h4>{{item.position}}</h4>
    <span> {{item.period}} </span>
    <p> {{item.description}} </p>
  {% endfor %}
</div>

<div class="section">
  <h2> {{ page.education.title }} </h2>
  {% for item in page.education.entries %}
    <h3> {{item.institutions}} </h3>
    <span>{{ item.type }}</span>
    <h4> {{item.period}} </h4>
    <p> {{item.name}} </p>
  {% endfor %}
</div>

<div style="margin-top: 30px; display: flex; justify-content: space-around; flex-wrap: wrap">
  {% for extra in page.extras %}
    <div>

    <h2 style="font-size: 2em; text-align: center; margin: 40px 0">{{extra.title}}</h2>

    {% for entry in extra.entries %}
      <p style="font-weight: bold">{{entry}}</p>
    {% endfor %}
    </div>
  {% endfor %}

</div>
