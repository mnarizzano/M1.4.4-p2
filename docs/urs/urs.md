
### UniSkaven UniApp
##### ITS ICT - Gruppo di Lavoro 2


**VERSION : 0.1**

**Authors**  
Serena Schincaglia
Federico Zunino

**REVISION HISTORY**

| Version    | Date        | Authors      | Notes        |
| ----------- | ----------- | ----------- | ----------- |
| 0.1 | 15/09/2022 | Federico| Update URS document, Part 1, 2, 3 tranne Functional Requirements |
| 0.1 | 15/09/2022 | Serena Schincaglia| Update URS document, Functional Requirements |
| 0.1 | 08/09/2022 | Serena Schincaglia, Federico Zunino | Tests Classi |
| 0.1 | 05/09/2022 | Federico Zunino | Creazione classi "Corso" e "Docente" e relative funzioni |
| 0.1 | 05/09/2022 | Serena Schincaglia | Creazione classi "Studente", "Voto", "Esame" e relative funzioni |


# Table of Contents

1. [Introduction](#p1)
	1. [Document Scope](#sp1.1)
	2. [Definitios and Acronym](#sp1.2) 
	3. [References](#sp1.3)
2. [System Description](#p2)
	1. [Context and Motivation](#sp2.1)
	2. [Project Objectives](#sp2.2)
3. [Requirement](#p3)
 	1. [Stakeholders](#sp3.1)
 	2. [Functional Requirements](#sp3.2)
 	3. [Non-Functional Requirements](#sp3.3)
  
  

<a name="p1"></a>

## 1. Introduction

<a name="sp1.1"></a>

### 1.1 Document Scope

Questo documento va ad illustrare gli update e i requisiti del progetto "UniSkaven UniApp" realizzato su commissione della Online University UniSkaven.

<a name="sp1.2"></a>

### 1.2 Definitios and Acronym


| Acronym				| Definition | 
| ------------------------------------- | ----------- | 
| XXXX                                  | XXXX |

<a name="sp1.3"></a>

### 1.3 References 

<a name="p2"></a>

## 2. System Description
<a name="sp2.15"></a>

### 2.1 Context and Motivation

Dopo aver esaminato l'offerta di software dedicati alla creazione e gestioni di corsi ed esami universitari, Uni-Skaven ha deciso di commissionare la realizzazione di un software proprietario che offrisse opzioni di scalability per il suo numero sempre crescente di studenti e personale, nonchè il futuro ampliamento della loro offerta formativa.

<a name="sp2.2"></a>

### 2.2 Project Obectives 

Il personale amministrativo Uni-Skaven poter creare profili unici per ogni studente e docente iscritto ad Uni-Skaven. L'amministrazione di UNI-Skaven creerà ed aggiungerà i corsi all'interno dei percorsi di laurea con i quasi si interfacceranno sia i docenti che gli studenti tramite browser o app dedicata. 

I docenti di Uni-Skaven potranno creare nuovi esami per i corsi da loro insegnati, interagire con la lista degli iscritti a ciascun esame e assegnare votazioni agli studenti che hanno sostenuto e passato l'esame.

Gli studenti Uni-Skaven potranno iscriversi e disiscriversi ai corsi, agli esami disponibili per ogni corso che non hanno già passato, e consultare la propria lista dei voti degli esami passati. 

<a name="p3"></a>

## 3. Requirements

| Priorità | Significato | 
| --------------- | ----------- | 
| M | **Mandatory:**   |
| D | **Desiderable:** |
| O | **Optional:**    |
| E | **future Enhancement:** |

<a name="sp3.1"></a>
### 3.1 Stakeholders

#### Utenti
| Gruppo | Ruoli |
| ----------- | ----------- | 
|Personale Amministrativo Uni-Skaven| Presidente Uni-Skaven, Direttori Dipartimenti, Personale Segreteria, Responsabile iscrizione Studenti, Responsabile immatricolazione Studenti, Responsabile di corso, Responsabile Borse di Studio|
|Personale Informatico Uni-Skaven| Amministratore di Sistema, Manutentore |
|Personale Scolastico Uni-Skaven| Docenti, Studenti |

#### Regolatori
| Gruppo | Ruoli |
| ----------- | ----------- | 
| Ufficio Legale "UnderCity" | Soci ufficio legale |

#### Clienti
| Nome | Descrizione |
| ----------- | ----------- | 
| Uni-Skaven | Committente del progetto |

<a name="sp3.2"></a>
### 3.2 Functional Requirements 

| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| 1.0 |  XXXXX |M|

<a name="sp3.3"></a>
### 3.3 Non-Functional Requirements 
 
| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| R1 | Il software deve essere compatibile con Windows, MACOS, e Linux |M|
| R2 | Il software deve essere accessibile tramite tutti i browser |M|
| R3 | Il software deve essere accessibile tramite app dedicata (Android e IoS) |S|
| R4 | Il software deve rispettare i dettami del GDPR |M|
| R5 | Il software deve appoggiarsi su un database dedicato |M|
| R6 | Il database deve avere back-up bigiornalieri sia in fisico che in cloud ai fini di una veloce disaster recovery |M|
| R7 | Il software deve essere disponibile anche in Inglese |M|
| R8 | Il software deve essere disponibile anche in Francese |D|
| R9 | Il software deve essere disponibile anche in Cinese Mandarino |D|
| R10 | Il software deve essere disponibile anche in Spagnolo |O|
| R11 | Il software deve essere disponibile anche in Tedesco|O|
| R12 | Il software deve essere disponibile anche in Arabo |O|