---
cssclass: research_note
type: "{{itemType}}"{% for type, creators in creators | groupby("creatorType") -%}{% if loop.first %}
{% endif %}{{type | replace("interviewee", "author") | replace("director", "author") | replace("presenter", "author") | replace("podcaster", "author") | replace("programmer", "author") | replace("cartographer", "author") | replace("inventor", "author") | replace("sponsor", "author")  | replace("performer", "author") | replace("artist", "author")}}: "{%- for creator in creators -%}{%- if creator.name %}{{creator.name}}{%- else %}{{creator.lastName}}, {{creator.firstName}}{%- endif %}{% if not loop.last %}; {% endif %}{% endfor %}"{% if not loop.last %}
{% endif %}{%- endfor %}{% if title %}
title: "{{title}}"{% endif %}{% if publicationTitle %}
publication: "{{publicationTitle}}"{% endif %}{% if date %}
date: {{date | format("YYYY-MM-DD")}}{% endif %}{% if archive %}
archive: "{{archive}}"{% endif %}{% if archiveLocation %}
archive-location: "{{archiveLocation}}"{% endif %}
citekey: {{citekey}}
aliases: 
    - "{{title}}"
---

# {{title}}

{{bibliography}}
[online]({{uri}}) [local]({{desktopURI}}) {%- for attachment in attachments | filterby("path", "endswith", ".pdf") %} [pdf](file://{{attachment.path | replace(" ", "%20")}})
{% if loop.last %} 
{% endif %}{%- endfor %}
 
{% persist "notes" -%}
{%- if isFirstImport %}

## My Thoughts

{% endif %}{% endpersist %}

### Annotations

{% persist "annotations" %}
{% set annotations = annotations | filterby("date", "dateafter", lastImportDate) -%}
{% if annotations.length > 0 %}
##### Imported on {{importDate | format("YYYY-MM-DD h:mm a")}}

{%- for annotation in annotations %}
{%- if annotation.type === "highlight" %}
>[!quote{% if annotation.color %}|{{annotation.color}}{% endif %}]
>{% if annotation.annotatedText %}{{annotation.annotatedText}} [(p. {{annotation.pageLabel}})](zotero://open-pdf/library/items/{{annotation.attachment.itemKey}}?page={{annotation.pageLabel}}&annotation={{annotation.id}}){%- endif %}
{%- if annotation.comment%}

>[!note]
>{{annotation.comment}}{%- endif %}
{%- endif -%}
{%- if annotation.type === "image" %}
##### <span style="color: {{annotation.color}}">Screenshot</span>
{% if annotation.imageRelativePath %}![[{{annotation.imageRelativePath}}]]{% endif %}

{%- endif -%}
{% if annotation.type === "note" %}
>[!note{% if annotation.color %}|{{annotation.color}}{% endif %}]
> {% if annotation.type === "note" %}{{annotation.comment}}{%- endif %}
{%- endif %}

---
{%- endfor %}{% endif %}{% endpersist %}

## Item Notes

{%- for note in notes %}

##### Note added on {{note.dateAdded | format("YYYY-MM-DD h:mm a")}}

{{note.note}}

{%- endfor %}

#### Tags

##### Keywords

{% if tags.length > 0 -%}{% for t in tags -%}#subject/{{t.tag | lower | replace(" ", "_")}}{% if not loop.last %} {% endif %}{%- endfor %}{%- endif %}

##### Authors

{% if creators.length > 0 -%}{%- for creator in creators -%}[[{%- if creator.name %}{{creator.name}}{%- else %}{{creator.firstName}} {{creator.lastName}}{%- endif %}]]{% if not loop.last %} {% endif %}{% endfor %}{%- endif %}

##### Publication

{% if journalAbbreviation %}#pub/{{journalAbbreviation | lower | replace(" ", "_")}}{%- else %}{% if publicationTitle %}#pub/{{publicationTitle | lower | replace(" ", "_")}}{% endif %}{% endif %}
