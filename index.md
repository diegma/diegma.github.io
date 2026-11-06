---
layout: default
---

<img class="portrait" src="{{ site.baseurl }}/img/people/diego.jpg" alt="Portrait of Diego Marcheggiani">

I'm a Senior Applied Scientist at Amazon in Barcelona, where I have worked since 2019.
Most recently I led the science for bringing customer review insights into the AI Overviews in Amazon search.
Before that I worked on the science behind the [AI-generated review highlights](https://www.aboutamazon.com/news/amazon-ai/amazon-improves-customer-reviews-with-generative-ai)
shown on Amazon product pages.
I also develop LLM-as-a-judge methods for evaluating LLMs, used both internally and in research
(see my EMNLP 2026 papers below), and mentor applied science interns.

Before Amazon I worked in NLP research. I was a researcher at ISTI-CNR in Pisa, where I also
did my PhD with the University of Venice, and then a postdoc with Ivan Titov at the University
of Amsterdam, including a visiting period at the University of Edinburgh.
More on my [About]({{ site.baseurl }}/about/) page and on [LinkedIn]({{ site.linkedin_url }}).

## Selected work

<ul class="work-list">
<li><a href="https://www.aboutamazon.com/news/amazon-ai/amazon-improves-customer-reviews-with-generative-ai">AI-generated review highlights</a><br><small>The "Customers say" summaries of customer reviews on Amazon product pages, in many languages and Amazon marketplaces worldwide.</small></li>
<li>AI Overviews in Amazon search<br><small>Bringing customer review insights into the AI Overviews in Amazon search.</small></li>
{%- assign highlights = "" | split: "" -%}
{%- for year in site.data.papers -%}{%- for paper in year[1] -%}{%- if paper.highlight == "y" -%}{%- assign highlights = highlights | push: paper -%}{%- endif -%}{%- endfor -%}{%- endfor -%}
{%- assign highlights = highlights | sort: "year" | reverse -%}
{%- for paper in highlights %}
<li><a {% if paper.doc-url %}href="{{ paper.doc-url }}"{% endif %}>{{ paper.title }}</a><br><small>{{ paper.authors }}. <i>{{ paper.booktitle }}{{ paper.journal }}</i>, {{ paper.year }}.</small></li>
{%- endfor %}
</ul>

[All publications &rarr;]({{ site.baseurl }}/publications.html)
