Academic publications that study environmentally sustainable artificial intelligence – **Green AI**.
In particular, this bibliography focus on research that aims at making the development of AI systems more friendly to the environment.

Contributions are welcome! If you have suggestions for other readings consider sending a pull request or creating an issue in the [Github repository][github-repo]!  😉

# Papers

{% for publication in site.publications reversed%}

{% assign currentdate = publication.year %}
{% if currentdate != date %}
### 📅 **{{ currentdate }}**
{% assign date = currentdate %} 
{% endif %}

  <p markdown="span">
      {{publication.author}} ({{publication.year}}).
      {%- unless publication.disable-page %}
      [**{{publication.title}}**]({{publication.url | relative_url}}).
      {%- else %}
      **{{publication.title}}**
      {%- endunless %}
      {%- if publication.journal %}
        *{{publication.journal}}*{% if publication.pages %} (pp. {{publication.pages}}){% endif %}.
      {% endif -%}
{%-for tag in publication.tags %}
<span class="badge">{{tag}}</span>
{% endfor %}
</p>
{%- if publication.annotation %}
<blockquote><small markdown="1">
{{publication.annotation | truncate: 300 }} [Read more.]({{publication.url | relative_url}})
</small></blockquote>
{% endif -%}

{% endfor %}


[github-repo]: https://github.com/luiscruz/green-ai
