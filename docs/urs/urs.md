### UniSkaven UniApp
##### ITS ICT - Gruppo di Lavoro 2

**VERSION : 0.1**

**Authors**  
Serena Schincaglia
Federico Zunino

**REVISION HISTORY**

| Version    | Date        | Authors      | Notes        |
| ----------- | ----------- | ----------- | ----------- |
| 0.1 | 22/09/2022 | Federico | Update Funzionalità Docente e Requisiti di Sistema |
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
| Gruppo | Ruoli | Obiettivo |
| ----------- | ----------- | ----------- |
|Personale Amministrativo Uni-Skaven| Presidente Uni-Skaven, Direttori Dipartimenti, Personale Segreteria, Responsabile iscrizione Studenti, Responsabile immatricolazione Studenti, Responsabile di corso, Responsabile Borse di Studio | Gestire organizzazione di iscrizioni, immatricolazioni, corsi nonchè il personale |
|Personale Informatico Uni-Skaven| Amministratore di Sistema, Manutentore | Poter verificare e modificare le funzionalità e i permessi del sistema |
|Personale Scolatisco Uni-Skaven| Docenti | Gestisce i corsi di cui è assegnato come docente, le liste degli studenti iscritti e gli appelli |
|Personale Scolatisco Uni-Skaven| Studenti | Gestisce i corsi a cui è iscritto, si iscrive agli esami e consulta i relativi voti |

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

#### 3.2.0 Requisiti Generali
| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| 0.1.0 | Ogni corso deve avere almeno 1 docente per essere considerato attivo e permettere iscrizioni studenti |M|
| 0.1.1 | I corsi non hanno un limite di docenti o studenti iscritti |M|
| 0.1.2 | Il sistema deve permettere agli utenti di segnalare errori |M|
| 0.1.3 | Un docente può registrare un voto per uno studente solo se è iscritto ad almeno un esame attivo del corso |M|
| 0.1.4 | Un docente non può registrare un voto ad uno studente che ha già un voto per il suo corso |M|
| 0.1.5 | Uno studente non può iscriversi ad un esame di un corso che ha già superato |M|

#### 3.2.1 Requisiti Funzionali Amministrazione

| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| 1.1.0 |  L'amministrazione crea profili docenti |M| 
| 1.1.1 |  L'amministrazione può modificare l'ID dei docenti |M|
| 1.1.2 |  L'amministrazione può modificare i dati anagrafici dei docenti |M| 
| 1.2.0 |  L'amministrazione crea profili studenti |M|
| 1.2.1 |  L'amministrazione può modificare l'ID degli studenti |M|
| 1.3.0 |  L'amministrazione crea corsi per ogni percorso di laurea |M|
| 1.4.0 |  L'amministrazione assegna i docenti ai corsi |M|

#### 3.2.2 Requisiti Funzionali Docenti

| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| 2.1.0 |  Il Docente può consultare la lista dei corsi che insegna |M| 
| 2.2.0 |  Il Docente può consultare la lista degli studenti iscritti ad un corso che insegna |M|
| 2.3.0 |  Il Docente visualizza elenco degli esami di un corso che insegna |M|
| 2.3.1 |  Il Docente può creare ed aggiungere un esame alla volta ad un corso che insegna |M|
| 2.3.2 |  Il Docente può rimuovere un esame alla volta da un corso che insegna |M|
| 2.3.3 |  Il Docente può spostare un esame alla volta in un corso che insegna |M|
| 2.4.0 |  Il Docente può verificare le sue informazioni di account - nome, cognome, id etc...|M|
| 2.4.1 |  Il Docente può modificare le sue informazioni di account - tranne l'ID |M|
| 2.5.0 |  Il Docente può consulare la lista degli studenti iscritti agli esami del suo corso |M|
| 2.6.0 |  Il Docente può assegnare una votazione ad ogni studente iscritto ad un suo esame |M|  

#### 3.2.3 Requisiti Funzionali Studenti

| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| 3.1.0 |  Lo Studente può consultare la lista dei corsi a cui è iscritto |M|
| 3.1.1 |  Lo Studente può consultare la lista dei corsi superati con relativa votazione |M|
| 3.2.0 |  Lo Studente può consultare la lista degli esami a cui è iscritto del suo corso |M|
| 3.2.1 |  Lo Studente può consultare la lista degli esami a cui può iscriversi |M|
| 3.3.0 |  Lo Studente può iscriversi a un esame alla volta ad un corso che frequenta |M|
| 3.3.1 |  Lo Studente può rimuovere un esame alla volta da un corso che frequenta |M|
| 3.4.0 |  Lo Studente può verificare le sue informazioni di account - nome, cognome, id etc...|M|



<a name="sp3.3"></a>
### 3.3 Non-Functional Requirements 
 
| ID | Descrizione | Priorità |
| --------------- | ----------- | ---------- | 
| R1 | Il software deve essere compatibile con Windows, MACOS, e Linux |M|
| R2 | Il software deve essere accessibile tramite tutti i browser |M|
| R3 | Il software deve essere accessibile tramite app dedicata (Android e IoS) |D|
| R4 | Il software deve rispettare i dettami del GDPR nell'acquisizione e protezione dei dati |M|
| R5 | Il software deve appoggiarsi su un database dedicato |M|
| R6 | Il database deve avere back-up bigiornalieri sia in fisico che in cloud ai fini di una veloce disaster recovery |M|
| R7 | Il software deve essere disponibile anche in Inglese |M|
| R8 | Il software deve essere disponibile anche in Francese |D|
| R9 | Il software deve essere disponibile anche in Cinese Mandarino |D|
| R10 | Il software deve essere disponibile anche in Spagnolo |O|
| R11 | Il software deve essere disponibile anche in Tedesco|O|
| R12 | Il software deve essere disponibile anche in Arabo |O|