---
layout: page
title: About
permalink: /
---

# [Get my CV](./resources/JQBung-CV-2024.pdf)

<br/>

<table>
  <tr>
    <td>
      <img class="profile_picture profile_picture_about" src="./resources/profile_pic.jpg" width="160" height="160" />
    </td>
    <td>
      I'm Jing Quan, Bung (you can just call me as Bung). I have 5 years of professional experience in backend API development, either in both microservices or modular architecture. I'm also working in DevOps tasks for 3 years. I have experience working on multiple cloud services. With the recent AWS Solution Achitect Associate certification, I am striving for software solution architect role to assist in designing complex, flexible, multi-leveleed system to enahce developing experience and end-user experience.
    </td>
  </tr>
</table>



# Employment History

<table>
{% for row in site.data.employment_history %}
    {% if forloop.first %}
        <tr>
          {% for pair in row %}
            <th>{{ pair[0] }}</th>
          {% endfor %}
        </tr>
    {% endif %}

    {% tablerow pair in row %}
        {{ pair[1] }}
    {% endtablerow %}

{% endfor %}

</table>

# Skills

1. Cloud Services
   - Amazon AWS
   - Microsoft Azure
   - Alibaba Cloud
   - Google Cloud Platform
2. Programming
   - JavaScripts/TypeScript
   - Python
   - C
   - Golang
3. DevOps Tools
   - Terraform
   - Ansible
   - Github Actions
   - Docker
   - Kubernetes
4. SVC Tools
   - JIRA
   - Trello
   - Linear
5. Infrastructure Framework
   - Proxmox
   - pfSense
   - OpenWRT

# Education & Achievements

- AWS Certified Solution Architect Associate - 2023
- BSc Hons Software Engineering, University of Nottingham Malaysia - First Class

# Get in touch

- jqbung0318@gmail.com

# Social Link

- [Twitter](https://twitter.com/jq_bung)
- [GitHub](https://github.com/jqbung0318)
- [LinkedIn](https://linkedin.com/in/jqbung-technies)
