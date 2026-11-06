---
layout: default
---

![Portrait of Diego Marcheggiani](/img/people/diego.jpg){: style="float: right; margin: 0px 20px; width: 250px; height: 229px" }

I'm a Senior Applied Scientist at Amazon in Barcelona, where I have worked since 2019.
I build NLP and large language model systems that ship in Amazon products,
most recently generative-AI review summaries on amazon.com.
My current focus is summarization, multilinguality, and the automatic evaluation of LLMs.
<!-- TODO: confirm the start year, team/area, and that the review-summaries project is OK to mention publicly. -->

Before Amazon I worked in NLP research. I did a PhD at the University of Venice and spent
several years at ISTI-CNR in Pisa, then held postdocs in Amsterdam and Edinburgh with Ivan Titov.
More in my [About]({{ site.baseurl }}/about/) page and my [CV]({{ site.baseurl }}/{{ site.cv }}).

### Selected publications

{% assign highlights = "" | split: "" -%}
{%- for year in site.data.papers -%}{%- for paper in year[1] -%}{%- if paper.highlight == "y" -%}{%- assign highlights = highlights | push: paper -%}{%- endif -%}{%- endfor -%}{%- endfor -%}
{%- assign highlights = highlights | sort: "year" | reverse -%}
<ul>
{%- for paper in highlights %}
<li><a {% if paper.doc-url %}href="{{ paper.doc-url }}"{% endif %}>{{ paper.title }}</a><br><small>{{ paper.authors }}. <i>{{ paper.booktitle }}{{ paper.journal }}</i>, {{ paper.year }}.</small></li>
{%- endfor %}
</ul>

[All publications &rarr;]({{ site.baseurl }}/publications.html)
