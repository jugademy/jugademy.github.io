---
meeting_date: TBA
meeting_authors: [piotr.ceranek]
title: Czy pisanie aplikacji webowych w sposób blokujący ma jeszcze sens?
old: false
layout: meeting
categories: [sezon-5]
image: assets/img/cover/czy-pisanie-aplikacji-webowych-w-sposob-blokujacy-ma-jeszcze-sens.png
---

Systemy informatyczne od zawsze musiały odpowiadać jak najszybciej. Jedna dziesiąta sekundy to dla użytkownika poczucie bezpośredniego manipulowania aplikacją. Jedna sekunda pozwala mu nadal niezakłócenie nawigować po interfejsie. Inny czas odpowiedzi jest nieodpowiedni. Dzisiejsze programy od początku powinny działać w sposób nieblokujący. 

Jak dostosować aplikacje tak by reagowały jak najszybciej, najlepiej w stałej puli zasobów i ze zwiększającym się wolumenem danych? Na to pytanie chciałbym odpowiedzieć pokazując jak te samą aplikację możemy napisać w sposób blokujący i nieblokujący, i jak zmierzyć performance tych aplikacji. Rozwiązanie pokaże z wykorzystaniem ugruntowanego narzędzia ze środowiska Javy (reactor), jak i nowego rozwiązania z Kotlina (coroutines).
