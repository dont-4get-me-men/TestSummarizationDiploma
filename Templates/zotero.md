## {{title}}
Author: {{authors}}
year: {{date | format ("YYYY")}}


### Notes
{% for annotation in annotations -%}{%- if annotation.annotatedText -%}{% if 'Red' in annotation.colorCategory %} 
##### {{annotation.annotatedText | escape }}{% else %}
<mark class="customZot-{% if annotation.color %}{{annotation.colorCategory}} {% endif %}">{{annotation.annotatedText | escape }}</mark> ([{{annotation.page}}](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.page}}&annotation={{annotation.id}}))

{% endif %}{%- endif %} {% if annotation.imageRelativePath %} ![[{{annotation.imageRelativePath}}]]{% endif %}{% if annotation.comment %} 
>{{annotation.comment}}
{% endif %}{% endfor -%}
