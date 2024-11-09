---
layout: archive
title: "Softwares"
permalink: /softwares/
author_profile: true
---

<style>
  /* Container for each software package block */
  .package-block {
    display: flex;
    flex-direction: column;
    border: 1px solid #ddd;
    padding: 1rem;
    margin-bottom: 1.5rem;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    background-color: #f9f9f9;
  }

  /* Title style for each package */
  .package-title {
    font-size: 1.2rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
  }

  /* Paper link and GitHub link styling */
  .package-links {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 0.5rem;
  }

  /* Paper link styling */
  .paper-link {
    font-style: italic;
    color: #555;
  }

  /* GitHub link styling */
  .github-link a {
    color: #0366d6;
    text-decoration: none;
    font-weight: bold;
  }
  
  .github-link a:hover {
    text-decoration: underline;
  }
</style>

R Packages:
-----
{% for post in site.research %}
<div class="package-block">
  <!-- Package title -->
  <div class="package-title">{{ post.title }}</div>
  
  <!-- Paper reference line (replace 'post.paper_reference' with actual paper reference variable) -->
  <div class="paper-link">Related Paper: {{ post.paper_reference }}</div>
  
  <!-- GitHub link section (replace 'post.github_url' with actual GitHub URL variable) -->
  <div class="package-links">
    <div class="github-link">GitHub: <a href="{{ post.github_url }}" target="_blank">{{ post.github_url }}</a></div>
  </div>
</div>
{% endfor %}
