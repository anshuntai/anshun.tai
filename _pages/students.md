---
layout: archive
title: "Students"
permalink: /students/
author_profile: true
---

<style>
  /* Main container for each student block */
  .student-block {
    margin-bottom: 1.5rem;
    border: 1px solid #ddd;
    padding: 1rem;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }

  /* Flex layout for blocks with photo */
  .has-photo .student-block {
    display: flex;
    align-items: flex-start;
  }

  /* Photo container */
  .photo {
    flex: 0 0 200px;
    margin-right: 1rem;
  }

  /* Photo styling */
  .photo img {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
  }

  /* Info container */
  .info {
    flex: 1;
  }

  /* No flex layout for blocks without photo */
  .no-photo .student-block {
    display: block;
    text-align: left;
  }

  /* Responsive styling */
  @media (max-width: 768px) {
    .student-block {
      flex-direction: column;
      align-items: center;
      text-align: center;
    }

    .photo {
      margin-bottom: 1rem;
      margin-right: 0;
    }

    .info {
      text-align: left;
    }
  }
</style>


Graduate (研究生):
-----
{% for student in site.data.students.graduate %}
<div class="{% if student.photo_url %}has-photo{% else %}no-photo{% endif %}">
  <div class="student-block">
    {% if student.photo_url %}
    <div class="photo">
      <img src="{{ student.photo_url }}" alt="Photo of {{ student.name }}">
    </div>
    {% endif %}
    <div class="info">
      <strong>{{ student.name }}</strong>  
      <br>{{ student.program }}, year {{ student.year }}
      <ul>
        <li>Research Interests: {{ student.research_interests }}</li> 
        <li>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></li> 
      </ul>
    </div>
  </div>
</div>
{% endfor %}

Undergraduate (專題生):
-----
{% for student in site.data.students.undergraduate %}
<div class="{% if student.photo_url %}has-photo{% else %}no-photo{% endif %}">
  <div class="student-block">
    {% if student.photo_url %}
    <div class="photo">
      <img src="{{ student.photo_url }}" alt="Photo of {{ student.name }}">
    </div>
    {% endif %}
    <div class="info">
      <strong>{{ student.name }}</strong>  
      <br>{{ student.department }}, year {{ student.year }}
      <ul> 
        <li>Research Interests: {{ student.research_interests }}</li>  
        <li>Research Title: "{{ student.research_title }}"</li>
        <li>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></li>
      </ul>
    </div>
  </div>
</div>
{% endfor %}

Alumni:
-----
{% for student in site.data.students.alumni %}
<div class="{% if student.photo_url %}has-photo{% else %}no-photo{% endif %}">
  <div class="student-block">
    {% if student.photo_url %}
    <div class="photo">
      <img src="{{ student.photo_url }}" alt="Photo of {{ student.name }}">
    </div>
    {% endif %}
    <div class="info">
      <strong>{{ student.name }}</strong>  
      <br>{{ student.program }}, {{ student.graduate_year }}  
      <ul>
        <li>Research Interests: {{ student.research_interests }}</li>
        <li>Thesis: {{ student.thesis }}</li>
        <li>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></li>
      </ul>
    </div>
  </div>
</div>
{% endfor %}

Research Assistant:
-----
{% for student in site.data.students.research_assistants %}
<div class="{% if student.photo_url %}has-photo{% else %}no-photo{% endif %}">
  <div class="student-block">
    {% if student.photo_url %}
    <div class="photo">
      <img src="{{ student.photo_url }}" alt="Photo of {{ student.name }}">
    </div>
    {% endif %}
    <div class="info">
      <strong>{{ student.name }}</strong>  
      <br>{{ student.department }}, year {{ student.year }}  
      <ul>
        <li>Research Interests: {{ student.research_interests }}</li>  
        <li>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></li>
      </ul>
    </div>
  </div>
</div>
{% endfor %}
