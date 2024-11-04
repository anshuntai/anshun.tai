---
layout: archive
title: "Students"
permalink: /students/
author_profile: true
---

<style>
  .student-block {
    display: flex;
    align-items: flex-start;
    margin-bottom: 1.5rem;
    border: 1px solid #ddd;
    padding: 1rem;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  
  .photo {
    flex: 0 0 100px;
    margin-right: 1rem;
  }
  
  .photo img {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: cover;
  }
  
  .info {
    flex: 1;
  }

  /* Responsive styling for smaller screens */
  @media (max-width: 768px) {
    .student-block {
      flex-direction: column;
      align-items: center;
      text-align: center;
    }
    
    .photo {
      margin-bottom: 1rem;
    }
    
    .info {
      text-align: left;
    }
  }
</style>

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
