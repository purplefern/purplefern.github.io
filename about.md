---
layout: page
title: About
permalink: /about/
---

<!-- Considerations for this post:
What is this site about?
Why does this site exist?
Who are you?
  What are your goals?
  What are your instruments?-->

_This page is an attempt to communicate the scope of this site's content, along with what I hope to get out of this site; additionally, I provide some information about myself, mostly pertaining to my interests_.

---

## About PurpleFern

PurpleFern is a pseudonym for my internet self. I prefer to keep my true identity mostly anonymous and fully reveal it only to a select few. I will share that I am a young American woman originally from the Southeastern US, currently residing in the Northeastern US, and that I studied chemistry in college.

## About This site

This site is a venue to share my art, my scientific research, and my writing about different topics. With a background in oil painting, I'm more recently experimenting with digital art and animation. As for research, I'm investigating topics in the fields of longevity and biosecurity with a special focus on collagen mutations and DNA synthesis screening.

## Contact

For inquiries, discussion, etc. contact me at _e.purplefern@gmail.com_

## Table of Contents
{:.no_toc}
* TOC
{:toc}

---

## This Site (Tags)

{% capture temptags %}
  {% for tag in site.tags %}
    #{{ tag[0] }}#
  {% endfor %}
{% endcapture %}
{% assign sortedtemptags = temptags | split:' ' | sort_natural %}
<ul>
{% for temptag in sortedtemptags %}
  {% assign tagitems = temptag | split: '#' %}
  {% capture tagname %}{{ tagitems[1] }}{% endcapture %}
  {% assign words = tagname | split: '-' %}
  {% capture titlecase %}
  {% for word in words %}
    {% if word.size <= 3 %}
      {{ word | upcase }}
    {% else %}
    {{ word | capitalize }}
    {% endif %}
  {% endfor %}{% endcapture %}
   <li style="display: inline-block; margin-right: 20px"><a href="/tag/{{ tagname }}"><em> {{ titlecase }} </em></a></li>
{% endfor %}
</ul>

&
