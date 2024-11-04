---
layout: archive
title: "Students"
permalink: /students/
author_profile: true
---

Graduate (研究生):
-----
{% for student in site.data.students.graduate %}
<div class="student-block">
  <div class="photo">
    ![Photo of {{ student.name }}]({{ student.photo_url }})
  </div>
  <div class="info">
    <strong>{{ student.name }}</strong>  
    <br>--- {{ student.program }}, {{ student.year }}  
    <br>**Research Interests**: {{ student.research_interests }}  
    <br>**Email**: <a href="mailto:{{ student.email }}">{{ student.email }}</a>
  </div>
</div>
{% endfor %}

Undergraduate (專題生):
-----
{% for student in site.data.students.undergraduate %}
<div class="student-block">
  <div class="photo">
    ![Photo of {{ student.name }}]({{ student.photo_url }})
  </div>
  <div class="info">
    <strong>{{ student.name }}</strong>  
    <br>--- {{ student.department }}, {{ student.year }}  
    <br>**Research Interests**: {{ student.research_interests }}  
    <br>**Email**: <a href="mailto:{{ student.email }}">{{ student.email }}</a>
    <br>**Research Title**: "{{ student.research_title }}"
  </div>
</div>
{% endfor %}

Research Assistant:
-----
{% for student in site.data.students.research_assistants %}
<div class="student-block">
  <div class="photo">
    ![Photo of {{ student.name }}]({{ student.photo_url }})
  </div>
  <div class="info">
    <strong>{{ student.name }}</strong>  
    <br>--- {{ student.department }}, {{ student.year }}  
    <br>**Research Interests**: {{ student.research_interests }}  
    <br>**Email**: <a href="mailto:{{ student.email }}">{{ student.email }}</a>
  </div>
</div>
{% endfor %}

Alumni:
-----
{% for student in site.data.students.alumni %}
<div class="student-block">
  <div class="photo">
    ![Photo of {{ student.name }}]({{ student.photo_url }})
  </div>
  <div class="info">
    <strong>{{ student.name }}</strong>  
    <br>--- {{ student.program }}, {{ student.year }}  
    <br>**Research Interests**: {{ student.research_interests }}  
    <br>**Email**: <a href="mailto:{{ student.email }}">{{ student.email }}</a>
  </div>
</div>
{% endfor %}
