> [!info]+ Metadata
> **Title**:: {{title}}
>
> **Author**:: {{authors}}; {{directors}}
> **Year**:: {{date | format ("YYYY")}}
>
> **Item Type**:: {{itemType | capitalize}}
> **Publisher**: {{publisher}}
> **Pages**:: {{numPages}}
>
> *Read start*::
> *Read end*::
> 
> **Tags**:: `{{hashTags}}` #source/zotero
> **Keywords**:: {{allTags}}
> **URL**:: {{url}}

> [!link]+ Zotero Link
>{{pdfZoteroLink}}

> [!abstract]+
> {{abstractNote}}

### Highlights
{% for annotation in annotations -%}
>[!Annotation|{{annotation.color}}]+
>#### ^{{annotation.id}}
>{%- if annotation.annotatedText -%}*« {{annotation.annotatedText}} »* ([Page {{annotation.page}}](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.page}}&annotation={{annotation.id}})){% endif %}{% if annotation.imageRelativePath %}![[{{annotation.imageRelativePath}}]][View on page {{annotation.page}}](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.page}}){% endif %}{% if annotation.comment %}
>
>{{annotation.comment}}{%- endif %}

{% endfor %}