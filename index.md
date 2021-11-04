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
      {%- if publication.booktitle %}
        In *{{publication.booktitle}}*{% if publication.pages %} (pp. {{publication.pages}}){% endif %}.
      {% endif -%}
      {%- if publication.journal %}
        *{{publication.journal}}*{% if publication.pages %} (pp. {{publication.pages}}){% endif %}.
      {% endif -%}
      {%- if publication.publisher %}{{publication.publisher}}.{% endif %}
      {%- if publication.award %}🏆 ***{{publication.award}}***.{% endif %}
      {%- if publication.preprint %} [Preprint]({{publication.preprint}}).{% endif %}
      {%- if publication.full-text %} [Full-text]({{publication.full-text}}).{% endif %}
      <!-- {%- if publication.bibtex %} <a class="clipboard" data-clipboard-text="{{publication.bibtex}}">Copy bibtex</a>.{% endif %} -->
      {%- if publication.slides %}
      [Slides]({{publication.slides}}.)
    {% endif -%}
  {%- if publication.video %}
    [<ion-icon name="logo-youtube"></ion-icon>]({{publication.video}})
  {% endif -%}
{%-for tag in publication.tags %}<span class="badge">{{tag}}</span>{% endfor %}
</p>
{%- if publication.annotation %}
> <small>{{publication.annotation | truncate: 300}} [Read more.]({{publication.url | relative_url}})</small>
{% endif -%}

{% endfor %}


[github-repo]: https://github.com/luiscruz/green-ai
