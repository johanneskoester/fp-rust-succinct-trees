# Fachprojekt: Entwicklung einer Rust-Bibliothek am Beispiel von Succinct Trees

_Johannes Köster, TU Dortmund, SS 2018_

Die Programmiersprache [Rust](https://www.rust-lang.org) erfreut sich in den letzten Jahren wachsender Beliebtheit. Neben tausenden Open-Source-Projekten erfolgt die derzeit stattfindende schrittweise Reimplementierung des Firefox-Browsers durch die Mozilla-Foundation in Rust. Des weiteren wurde Rust zwei Jahre in Folge zur ["most loved programming language"](https://insights.stackoverflow.com/survey/2017) auf Stack Overflow gewählt. Ein Grund für diese Beliebtheit ist der Compiler von Rust, der es erlaubt Thread- und Speichersicherheit zur Kompilierzeit zu garantieren ohne Geschwindigkeitseinbußen hinnehmen zu müssen. Dies ist realisiert indem Speicherallokationen und -zugriffe einem neuartigen Konzept von "Ownership" und "Borrowing" unterworfen werden.

Ziel des Fachprojekts ist, mittels Rust eine robuste und schnelle Implementierung von [Succinct Trees](https://dl.acm.org/citation.cfm?id=2790240) als Programmierbibliothek zu realisieren. Durch die Verwendung von Bitvektor-Techniken \(Rank/Select\) ermöglichen Succinct Trees die Repräsentation von Bäumen mit $$n$$ Knoten in $$2n + o(n)$$ Bits anstelle von $$O(n \log n)$$ Bits. Des weiteren können diverse Baum-Operationen in konstanter Zeit ausgeführt werden. Eine erfolgreiche Implementierung besäße zahlreiche Anwendungsmöglichkeiten, insbesondere in Fällen wo eine herkömmliche Baumrepräsentation nicht effizient genug oder zu groß wäre.

Es existieren mehrere alternative Repräsentationen von succinct trees, die je nach Operation unterschiedliche Stärken und Schwächen haben. Die Aufgabe der Studenten ist, mindestens eine Repräsentation zu implementieren. Dabei wird zum einen ein Einblick in ein neues theoretisches Feld, zum anderen in eine vielversprechende neue Programmiersprache gewonnen. Des weiteren hat sich gezeigt, dass die Beschäftigung mit den Konzepten von Rust hilft, ein besseres Verständnis für wichtige technische Aspekte der Programmierung zu entwickeln.

## Plan

Das Fachprojekt ist in drei Phasen gegliedert.

1. **Erlernen von Rust.** Dies geschieht durch das Studium der [offiziellen Dokumentation](https://doc.rust-lang.org/book/second-edition/) gepaart mit praktischen Übungen. Hierzu werden 2er-Gruppen gebildet.
2. **Erarbeiten verschiedener Varianten von Succinct Trees.** Dies geschieht in 3er-Gruppen.
3. **Implementierung von Succinct Trees als Rust-Bibliothek.** Dies geschieht ebenfalls in 3er-Gruppen, wobei die Gruppenmitglieder zuvor in unterschiedlichen Gruppen gewesen sein müssen.

| Tag | Thema |
|-----|-------|
| 13.04.2018 | Einführung in Rust, Verteilung der 6 Vortragsthemen (3er-Gruppen), praktische Übungen |
| 20.04.2018 | Praktische Übungen |
| 27.04.2018 | Praktische Übungen |
| 04.05.2018 | Vorbereitung der Vorträge |
| 11.05.2018 | Vorbereitung der Vorträge |
| 18.05.2018 | Vorträge (je 30min) |
| 25.05.2018 | Implementierung der Rust-Bibliothek |
| 01.06.2018 | Implementierung der Rust-Bibliothek |
| 08.06.2018 | Implementierung der Rust-Bibliothek |
| 15.06.2018 | Implementierung der Rust-Bibliothek |
| 22.06.2018 | Implementierung der Rust-Bibliothek |
| 29.06.2018 | Implementierung der Rust-Bibliothek |
| 06.07.2018 | Implementierung der Rust-Bibliothek |
| 13.07.2018 | Vorbereitung der Abschlusspräsentationen |
| 20.07.2018 | Abschlusspräsentationen |