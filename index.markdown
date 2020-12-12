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
    <h2>{{ meeting.meeting_title }} <small>{{ meeting.meeting_date }}</small></h2>
    <section>
    <p>{{ meeting.meeting_author }}</p>
    {{ meeting.content | markdownify }}
    </section>
    {% endfor %}
</div>

# Nagrody

- kody na [Pyszne.pl](https://pyszne.pl)
- książy wydawnictwa [Helion](https://helion.pl/)

# Sponsorzy

[![Allegro Tech](https://allegro.tech/img/allegro-tech.svg)](https://allegro.tech)