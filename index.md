---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
{%- if site.posts.size > 0 -%}
    <ul>
        {%- for post in site.posts -%}
        <li>
            {%- assign date_format = "%Y-%m-%d" -%}
            [ {{ post.date | date: date_format }} ] <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
        </li>
        {%- endfor -%}
    </ul>
{%- endif -%}