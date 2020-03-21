---
layout: page
title: Afghanistan Blog
---

During 2012, I spent the better part of six months working as a contractor for the US Army in Afghanistan. I wrote a lot about my work, living conditions, and my other experiences and adventures while I was there to help stay connected with friends and family back home. Here you can find an archive of the blog posts that I wrote during that time.

I also compiled an [FAQ](/pages/afghanistan-faqs) page and a collection of [Acronyms of the Day (AOTD)](/pages/afghanistan-aotd).

<ul class="posts">

    <ul class="post-list">
        {% for post in site.afghanistan %}
        <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <span class="post-meta">{{ post.date | date: date_format }}</span>
        <h3>
            <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
            </a>
        </h3>
        {%- if site.show_excerpts -%}
            {{ post.excerpt }}
        {%- endif -%}
        </li>
        {%- endfor -%}
    </ul>

</ul>