---
layout: jugademy
---

# Sezon 4

W 2021 roku startujemy z 4 sezonem. Już niedługo podzielimy się z Wami informacjami, kogo i gdzie
będziecie mogli posłuchać. Sezon ten jest w pełni zdalny, ale nie martwcie się. Także tym razem
przewidzieliśmy [nagrody](#nagrody) dla najbardziej aktywnych uczestników! Więcej informacji już wkrótce!

# Terminarz

<div>
    {% for meeting in site.meetings %}
    <section>
        <h2 id="{{meeting.meeting_title | slugify }}">
            <a href="#{{ meeting.meeting_title | slugify }}">{{meeting.meeting_title}}</a>
            <small>{{ meeting.meeting_date }}</small>
        </h2>
        {{ meeting.content | markdownify }}
        
        {% for author in meeting.meeting_authors %}
            {% if site.data.authors[author] %}
            {% assign meeting_author = site.data.authors[author] %}

            <p><span class="meeting-author">{{ meeting_author.name }}</span> &ndash; {{ meeting_author.bio }}</p>
        
            {% endif %}
        {% endfor %}
        
        {% if meeting.meeting_link %}
            {{ meeting.meeting_link | markdownify }}
        {% endif %}
    </section>
    {% endfor %}
</div>

# Nagrody

- kody na [Pyszne.pl](https://pyszne.pl)
- książki wydawnictwa [Helion](https://helion.pl/)

# Partnerzy

[![Allegro Tech](https://allegro.tech/img/allegro-tech.svg)](https://allegro.tech)

[![Politechnika Poznańska](http://www.nzs.put.poznan.pl/wp-content/uploads/Politechnika-Pozna%C5%84ska.png)](https://www.put.poznan.pl/)