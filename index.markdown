---
layout: jugademy
---

# Sezon 4

W 2021 roku startujemy z 4 sezonem. Już niedługo podzielimy się z Wami informacjami, kogo i gdzie
będziecie mogli posłuchać. Sezon ten jest w pełni zdalny, ale nie martwcie się. Także tym razem
przewidzieliśmy [nagrody](#nagrody) dla najbardziej aktywnych uczestników!

Zobacz, co przed nami lub dowiedz się więcej o:
 - [Przeszłe prezentacje](#przeszłe-prezentacje)
 - [Nagrody](#nagrody)
 - [Partnerzy](#partnerzy)

{% assign new_posts = site.meetings | where: "old","false" %}
{% assign old_post = site.meetings | where: "old","true" %}
{% assign new_posts_size = new_posts | size %}
{% assign old_posts_size = new_posts | size %}

{% if new_posts_size > 0 %}
# Nadchodzące spotkania

<div>
    
    {% for meeting in new_posts %}
        {% include meeting.html meeting=meeting %}
    {% endfor %}
</div>

{% else %}

# Za nami wszystkie spotkanie tego sezonu

Do zobaczenia jesienią

{% endif %}

{% if old_post %}

# Przeszłe prezentacje

<div>
    <ul>
   
    {% for meeting in old_post %}
        <li>
            <a href="{{ meeting.url }}">{{ meeting.title }} &ndash;
            {% assign meeting_authors_size = meeting.meeting_authors | size %}
            {% for author in meeting.meeting_authors %}
                {% if site.data.authors[author] %}
                {% assign meeting_author = site.data.authors[author] %}
                <span class="meeting-author">
                    {{ meeting_author.name }}{%if forloop.last == false %},{%endif%}
                </span>
                {% endif %}
            {% endfor %}
            </a>
        </li>
    {% endfor %}
    </ul>
</div>

{% endif %}

# Nagrody

- kody na [Pyszne.pl](https://pyszne.pl)
- książki wydawnictwa [Helion](https://helion.pl/)

# Partnerzy

[![Allegro Tech](https://allegro.tech/images/logo.svg)](https://allegro.tech)

[![Politechnika Poznańska](/assets/img/politechnika-poznanska.png)](https://www.put.poznan.pl/)