> ## Contents
> {% for cat in site.category-list %}
> {% if cat == 'torrent-remote' %}
> <ul>
>   {% for page in site.pages %}
>     {% if page.resource == true %}
>       {% for pc in page.categories %}
>         {% if pc == cat %}
>           <li><a href="/docs/{{ page.url }}">{{ page.title }}</a></li>
>         {% endif %}   
>       {% endfor %}  
>     {% endif %}   
>   {% endfor %}  
> </ul>
> {% endif %}
> {% endfor %} 
