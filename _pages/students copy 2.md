---
layout: archive
title: "Students"
permalink: 
author_profile: true
---

<style>
  /* Main container for each student block */
  .student-block {
    /* Use flexbox to align photo and info side-by-side */
    display: flex;
    /* Align items at the top for a clean, aligned look */
    align-items: flex-start;
    /* Add spacing between student blocks */
    margin-bottom: 1.5rem;
    /* Light border around each block for separation */
    border: 1px solid #ddd;
    /* Add padding inside the block for visual breathing room */
    padding: 1rem;
    /* Rounded corners for a softer look */
    border-radius: 8px;
    /* Subtle shadow to make the block stand out */
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  
  /* Container for the student's photo */
  .photo {
    /* Fix the size of the photo container to 100px wide */
    flex: 0 0 200px;
    /* Space between the photo and the info section */
    margin-right: 1rem;
  }
  
  /* Style for the photo image itself */
  .photo img {
    /* Set the image dimensions to a square */
    width: 200px;
    height: 200px;
    /* Make the image circular for a profile-like appearance */
    border-radius: 50%;
    /* Ensures the image covers the entire area and is centered */
    object-fit: cover;
  }
  
  /* Container for the student's information */
  .info {
    /* Allow the info section to expand and take up available space */
    flex: 1;
  }

  /* Responsive styling for screens 768px wide or smaller */
  @media (max-width: 768px) {
    .student-block {
      /* Stack the photo and info vertically for better readability on small screens */
      flex-direction: column;
      /* Center-align items for a cleaner, mobile-friendly appearance */
      align-items: center;
      /* Center-align text for consistency in mobile layout */
      text-align: center;
    }
    
    /* Adjust photo spacing for stacked layout */
    .photo {
      /* Add space below the photo to separate it from the info */
      margin-bottom: 1rem;
      /* Center-align the photo in the stacked layout */
      margin-right: 0;
    }
    
    /* Align info text back to the left on mobile if needed */
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
    <img src="{{ student.photo_url }}" alt="Photo of {{ student.name }}">
  </div>
  <div class="info">
    <strong>{{ student.name }}</strong>  
    <br>{{ student.program }}, year {{ student.year }}
    <ul>
      <li>Research Interests: {{ student.research_interests }}</li> 
      <li>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></li> 
    </ul>
  </div>
</div>
{% endfor %}


Undergraduate (專題生):
-----
{% for student in site.data.students.undergraduate %}
<div class="student-block">
  <div class="photo">
    <img src="{{ student.photo_url }}" alt="Photo of {{ student.name }}">
  </div>
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
{% endfor %}


Alumni:
-----
{% for student in site.data.students.alumni %}
<div class="student-block">
  <div class="photo">
    <img src="{{ student.photo_url }}" alt="Photo of {{ student.name }}">
  </div>
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
{% endfor %}


Research Assistant:
-----
{% for student in site.data.students.research_assistants %}
<div class="student-block">
  <div class="photo">
    <img src="{{ student.photo_url }}" alt="Photo of {{ student.name }}">
  </div>
  <div class="info">
    <strong>{{ student.name }}</strong>  
    <br>{{ student.department }}, year {{ student.year }}  
    <ul>
      <li>Research Interests: {{ student.research_interests }}</li>  
      <li>Email: <a href="mailto:{{ student.email }}">{{ student.email }}</a></li>
    </ul>
  </div>
</div>
{% endfor %}