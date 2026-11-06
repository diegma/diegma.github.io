---
layout: default
---

![Portrait of Diego Marcheggiani](/img/people/diego.jpg){: style="float: right; margin: 0px 20px; width: 250px; height: 229px" }

I'm a Senior Applied Scientist at Amazon in Barcelona, where I have worked since 2019.
Since joining I have worked on extracting and summarizing information from customer reviews,
including four years on the science behind the [AI-generated review highlights](https://www.aboutamazon.com/news/amazon-ai/amazon-improves-customer-reviews-with-generative-ai)
shown on Amazon product pages.
I also mentor interns and do applied research, currently on the automatic evaluation of LLMs
(see my EMNLP 2026 papers below). My interests include summarization, multilinguality, and LLM evaluation.

Before Amazon I worked in NLP research. I was a researcher at ISTI-CNR in Pisa, where I also
did my PhD with the University of Venice, and then a postdoc with Ivan Titov at the University
of Amsterdam, including a visiting period at the University of Edinburgh.
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
