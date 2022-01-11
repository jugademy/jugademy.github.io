---
layout: jugademy
image: assets/img/cover/index.png
---

# Witaj


{% assign new_posts = site.meetings | where: "old","false" %}
{% assign old_post = site.meetings | where: "old","true" %}
{% assign new_posts_size = new_posts | size %}
{% assign old_posts_size = new_posts | size %}

Zobacz, co przed nami lub dowiedz się więcej o:
 - [planach na 2022 rok]
{% if new_posts_size > 0 %}- [nadchodzących prezentacjach](#nadchodzące-spotkania){% endif %}
 - [przeszłych prezentacjach](#przeszłe-prezentacje)
 - [nagrodach dla uczestników](#nagrody-dla-uczestników)
 - [naszych partnerach](#partnerzy)


{% if new_posts_size > 0 %}
# Nadchodzące spotkania

<div>
    
    {% for meeting in new_posts %}
        {% include meeting.html meeting=meeting %}
    {% endfor %}
</div>

{% else %}

# Za nami wszystkie spotkanie tego sezonu

Do zobaczenia wkrótce!

{% endif %}

{% if old_post %}

# Przeszłe prezentacje

<div>
    <ul>
   
    {% for meeting in old_post %}
        <li class="old-meetings">
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

# Nagrody dla uczestników

- kody na [Pyszne.pl](https://pyszne.pl)

# Partnerzy

[![Allegro Tech](https://allegro.tech/images/logo.svg)](https://allegro.tech)

[![Politechnika Poznańska](/assets/img/politechnika-poznanska.png)](https://www.put.poznan.pl/)

<script>
(function(){var hash=window.location.hash;var matches={"#wprowadzenie-do-mongodb":"/spotkania/sezon-4/wprowadzenie-do-mongodb","#czysty-kod-to-wcale-nie-jest-takie-trudne":"/spotkania/sezon-4/czysty-kod-to-wcale-nie-jest-takie-trudne","#programowanie-funkcyjne-na-jvm":"/spotkania/sezon-4/programowanie-funkcyjne-na-jvm","#praca-z-danymi-w-apache-spark":"/spotkania/sezon-4/praca-z-danymi-w-apache-spark","#ogarnąć-git-a":"/spotkania/sezon-4/ogarnac-git-a","#reaktywne-aplikacje-od-podstaw":"/spotkania/sezon-4/reaktywne-aplikacje-od-podstaw","#wprowadzenie-do-rest-api":"/spotkania/sezon-4/wprowadzenie-do-rest-api","#kotlin-dlaczego-warto-spróbować-od-czego-zacząć":"/spotkania/sezon-4/kotlin-dlaczego-warto-sprobowac-od-czego-zaczac","#wprowadzenie-do-cassandry":"/spotkania/sezon-4/wprowadzenie-do-cassandry","#jednoosobowy-pair-programing-czyli-twoja-wydajność-w-intellij-idea":"/spotkania/sezon-4/jednoosobowy-pair-programming-czyli-twoja-wydajnosc-w-intellij-idea","#abstractqueuedsynchronizer-the-cornerstone-of-java-concurrency":"/spotkania/sezon-4/abstractqueuedsynchronizer-the-cornerstone-of-java-concurrency"};for(var i in matches){matches[encodeURI(i)]=matches[i];}if(matches.hasOwnProperty(hash)){window.location.replace(matches[hash])}})();
</script>

[planach na 2022 rok]: /start-2022
