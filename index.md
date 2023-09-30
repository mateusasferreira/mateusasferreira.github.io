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
      period: Jun/2022 - ongoing
      description: >
        Aliqua consequat est sunt irure. Occaecat et minim sunt consectetur voluptate minim cillum culpa. Duis proident officia labore aliquip ea proident quis magna eiusmod magna. Anim est cillum tempor nulla culpa anim.
    - name: Anbetec
      period: Feb/2022 - May/2022
      description: >
        Aliqua consequat est sunt irure. Occaecat et minim sunt consectetur voluptate minim cillum culpa. Duis proident officia labore aliquip ea proident quis magna eiusmod magna. Anim est cillum tempor nulla culpa anim.
    - name: Haittane
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
---

# {{ page.title }}

### {{page.description}}

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
    <h4> {{item.period}} </h4>
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


