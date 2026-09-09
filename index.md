---
layout: page
cover-img: /assets/images/coriolis-reunion.jpg
---

At CERMICS, we organize roughly every two weeks a seminar for the young researchers, ranging from interns to post-docs. The subject and the format of the presentation are varied, and the seminar is open to everyone who is interested : if you are external to the lab, contact one of the organizers to arrange your visit !

### Organizers of the seminar
<a href="https://nailbaloul.github.io/" target="_blank">Nail Baloul</a>, 
<a href="https://team.inria.fr/matherials/team-members/clement-guillot/" target="_blank">Clement Guillot</a>,
<a href="https://setar0202.github.io/" target="_blank">Seta Rakotomandimby</a>,
<a href="https://sites.google.com/view/rosesossouedou/home" target="_blank">Rose Sossou Edou</a>.

### Forthcoming presentations and events
(<a href="https://framagenda.org/apps/calendar/p/QRrqeeZa2jWenYMA" target="_blank">Schedule</a>)

{% for link in site.data.young-researchers %}
{% if link.next == "yes" %}
{% if link.sem == "scommun" %}
 {{ link.date | date : "%A, %B %-d, %Y" }} {% if link.hour != "void" %}, {{ link.hour }}{% endif %}: **{{ link.AU }}**,  
{{ link.labo }}  
*{{ link.TI }}
{% for sublink in link.PROG %}
 - {{ sublink.hour }}: **{{ sublink.AU }}**,  
*{{ sublink.TI }}*.  
{{ link.where }}
{% endfor %}
{% else %}
{{ link.date | date : "%A, %B %-d, %Y" }}{% if link.hour != "void" %}, {{ link.hour }}{% endif %}: **{{ link.AU }}**, {{ link.labo }}  
*{{ link.TI }}*{% if link.slides %}, <a href="{{ link.slides | relative_url }}">(slides)</a>{% endif %}{% if link.recording %}, <a href="{{ link.recording }}">(recording)</a>{% endif %}.  
{{ link.where }}
{% endif %}
-------------------------
{% endif %}
{% endfor %}

### Past presentations and events
{% assign year = "3000" %}

{% for link in site.data.young-researchers %}
{% if link.next != "yes" %}
{% assign link_year = link.date | date : "%Y" %}
{% if link_year != year %}{% assign year = link_year %}<h3>{{ year }}</h3>{% endif %}
{% if link.sem == "scommun" %}
{{ link.date | date : "%A, %B %-d, %Y" }}{% if link.hour != "void" %}, {{ link.hour }}{% endif %}: **{{ link.AU }}**, {{ link.labo }}  
*{{ link.TI }}
{% for sublink in link.PROG %}
 - {{ sublink.hour }}: **{{ sublink.AU }}**,  
*{{ sublink.TI }}*.  
{{ link.where }}
{% endfor %}
{% else %}
{{ link.date | date : "%A, %B %-d, %Y" }}{% if link.hour != "void" %}, {{ link.hour }}{% endif %}: **{{ link.AU }}**, {{ link.labo }}  
*{{ link.TI }}*{% if link.slides %}, <a href="{{ link.slides | relative_url }}">(slides)</a>{% endif %}{% if link.recording %}, <a href="{{ link.recording }}">(recording)</a>{% endif %}.  
{{ link.where }}
{% endif %}
-------------------------
{% endif %}
{% endfor %}


