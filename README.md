![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-darkslategray?style=for-the-badge&logo=caddy&logoColor=green)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=for-the-badge&logo=Raspberry%20Pi&logoColor=white)

# Kalender

Software-Stack zur Verwaltung unserer Kalender.
Speziell für einen Raspberry-Pi.

Realisiert wird das ganze über Caddy, ein Reverse-Proxy, welcher in Docker läuft.
Dieser wertet die Anfragen aus und leitet diese entweder an einen general-purpose Webserver, oder an die Kalenderverwaltung weiter.

## iCalendar

Unsere Kalender werden mit Google Calendar verwaltet.
Für jede Kategorie (Übungen, Termine zur Instandhaltung, ...) gibt es einen eigenen Kalender.
Damit diese automatisch aktualisiert werden und unsere Mitglieder leicht darauf zugreifen können, verwenden wir https://github.com/Jojodicus/calunite.
Mit dem Tool wird auch gleichzeitig ein gesammelter Kalender erstellt, damit man bei Bedarf nicht jeden Kalender einzeln abonnieren muss.

## Webserver

Anfragen, die nicht an ein Kalenderabo gehen, werden mit einem dedizierten Webserver verwaltet.
Stand jetzt hostet dieser nur eine entsprechende Anleitung fürs Abonnieren (ähnlich https://github.com/Jojodicus/calunite).
In Zukunft kann und soll dort aber eine interaktive Website für unsere Kalender entstehen.
