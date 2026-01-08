# Woche 1 Kata – Relationale Grundlagen & JPA Entity Lifecycle

## Ziel des Katas

Dieses Kata dient dazu, grundlegende **Senior-relevante Kompetenzen** im Umgang mit relationalen Datenbanken und JPA zu trainieren.

Der Fokus liegt **nicht** auf komplexer Business-Logik, sondern auf:

- sauberer relationaler Modellierung
- bewussten JPA-Entscheidungen
- Verständnis des Entity Lifecycles
- kontrolliertem Umgang mit dem Persistence Context
- Wartbarkeit und Skalierbarkeit des Datenmodells

---

## Fachlicher Kontext

Das Projekt implementiert ein vereinfachtes **Order-Management-System** für einen Online-Shop.

Ein Kunde kann Bestellungen aufgeben.  
Eine Bestellung besteht aus mehreren Positionen, die sich auf Produkte beziehen.

Der fachliche Umfang ist bewusst klein gehalten, um den Fokus auf **Datenmodell, Beziehungen und JPA-Verhalten** zu legen.

---

## Funktionale Anforderungen

- Ein **Customer** kann mehrere **Orders** besitzen
- Eine **Order** besteht aus mehreren **OrderItems**
- Ein **OrderItem** referenziert genau ein **Product**
- Eine **Order** besitzt:
  - einen Erstellungszeitpunkt
  - einen Status (z. B. `CREATED`, `PAID`)
- **Products** sind unabhängig vom Lifecycle einer Order

---

## Nicht-funktionale Anforderungen

- Saubere relationale Normalisierung
- Klare Primary- und Foreign-Key-Strategie
- Keine unnötig großen Objektgraphen
- Kontrolliertes Laden von Entitäten
- Verständliche, wartbare Code-Struktur
- Tests, die reales Persistenzverhalten abdecken

---

## Technischer Stack

- Java oder Kotlin
- Spring Boot
- JPA (Hibernate)
- Relationale Datenbank (lokal z. B. H2)

---

## Technischer Fokus

Dieses Kata konzentriert sich insbesondere auf:

- JPA Entity Lifecycle (`transient`, `managed`, `detached`)
- Verhalten des Persistence Contexts
- Auswirkungen von Beziehungen auf Performance
- Trade-offs bei Mapping-Entscheidungen
- Vermeidung typischer ORM-Fallen

---

## Bewusste Einschränkungen

Um den Lernfokus zu schärfen, werden folgende Dinge **bewusst vermieden**:

- `@Data` oder ähnliche Lombok-Alleskönner auf Entities
- Unnötige bidirektionale Beziehungen
- `CascadeType.ALL` ohne fachliche Begründung
- Eager Loading als Default
- Business-Logik, die vom ORM-Verhalten abhängt

---

## Qualitätskriterien (Senior-Level)

Die Lösung gilt als **Senior-tauglich**, wenn:

- Architektur und Layer klar getrennt sind
- Beziehungen

