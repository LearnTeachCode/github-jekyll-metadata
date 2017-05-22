---

---

<p>Testing from <a href="https://help.github.com/articles/repository-metadata-on-github-pages/">https://help.github.com/articles/repository-metadata-on-github-pages/</a>.

<p><strong>owner_name:</strong> {{ site.github.owner_name }}</p>
<p><strong>owner_url:</strong> {{ site.github.owner_url }}</p>
<p><strong>owner_gravatar_ url:</strong> {{ site.github.owner_gravatar_url }}</p>

<p><strong>project_title:</strong> {{ site.github.project_title }}</p>
<p><strong>project_tagline:</strong> {{ site.github.project_tagline }}</p>

<p><strong>repository_name:</strong> {{ site.github.repository_name }}</p>
<p><strong>repository_url:</strong> {{ site.github.repository_url }}</p>

<img src="{{ site.github.owner_gravatar_url }}">

<h2>List of repos in this organization:</h2>
{% for repository in site.github.public_repositories %}
  * [{{ repository.name }}]({{ repository.html_url }})
{% endfor %}

<h2>List of members in this organization:</h2>
{% for member in site.github.organization_members %}
  * name: {{ member.name }}
  * login: {{ member.login }}
  * html_url: {{ member.html_url }}
  * avatar_url: {{ member.avatar_url }}
  <img src="{{ member.avatar_url }}">
{% endfor %}

<h2>List of contirbutors to this repo:</h2>
{% for member in site.github.contributors %}
  * name: {{ member.name }}
  * login: {{ member.login }}
  * html_url: {{ member.html_url }}
  * avatar_url: {{ member.avatar_url }}
  <img src="{{ member.avatar_url }}">
{% endfor %}
