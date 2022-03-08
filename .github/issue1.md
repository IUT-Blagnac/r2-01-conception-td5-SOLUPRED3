---
title: Exercice 1 : Diagramme des UC en plantUML ({{ date | date('dddd, MMMM Do') }})
---
En vous inspirant du code suivant (pour ne pas démarrer à vide), réalisez un diagramme des UC correspondant au sujet.
```plantuml
@startuml

usecase r as "Recenser les \n demandes de stage"
usecase d as "Déclarer une \n demande de stage"
usecase p as "Participer à un chantier"
usecase g as "Gérer les artisans"
usecase pa as "Payer les artisans"

actor Responsable
actor Entreprise 
actor Artisan

'Pour aligner les 3 acteurs :
r -[hidden]-> d
d -[hidden]-> g
g -[hidden]-> pa
pa -[hidden]-> p

Responsable -> r
Entreprise -> d
Artisan -> p
Entreprise -> g
Entreprise -> pa

@enduml
```