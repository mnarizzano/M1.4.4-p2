### UniSkaven UniApp
##### ITS ICT - Gruppo di Lavoro 2

**VERSION : 0.1**

**Authors**  
Serena Schincaglia
Federico Zunino
Tiziano De Falco

**REVISION HISTORY**

| Version    | Date        | Authors      | Notes        |
| ----------- | ----------- | ----------- | ----------- |
|0.1| 22/09 | Seren, Federico, Tiziano | Update lista funzionalità e scenario 1 to 5 |
|0.1| 22/09 | Federico Zunino | Creazione documento srs, update lista attori|

# Table of Contents

1. [User Case](#p1)
	1. [Diagramma](#sp1.1)
	2. [Attori](#sp1.2) 
	3. [Lista Funzionalità](#sp1.3)
2. [Scenari](#p2)
	1. [Login](#sp2.1)
	2. [Consulta Lista Corsi](#sp2.2)
	3. [Lista Studenti iscritti al corso](#sp2.3)
	4. [Elenco Esami Attivi Corso](#sp2.4)
	5. [Aggiunta Esame Corso](#sp2.5)
	6. [](#sp2.6)
	7. [](#sp2.7)
	8. [](#sp2.8)
	9. [](#sp2.9)
	10. [](#sp2.10)
	11. [](#sp2.11)
	12. [](#sp2.12)
	13. [](#sp2.13)
	14. [](#sp2.14)
	15. [](#sp2.15)
	16. [](#sp2.16)
	17. [](#sp2.17)
	18. [](#sp2.18)
	19. [](#sp2.19)
	20. [](#sp2.20)
	21. [](#sp2.21)
	22. [](#sp2.22)

<a name="p1"></a>

## 1. User Case

<a name="sp1.1"></a>

### 1.1 Diagramma

<a name="sp1.2"></a>

### 1.2 Attori

| Nome | Descrizione |
| ----------- | ----------- | 
|Studente| Utente frequentante i corsi di Skaven University e che passa esami fino alla laurea |
|Docente| Utente che insegna uno o più corsi a Skaven Univerisity e esamina gli Studenti |
|Amministrazione| Utente generale dell'amministrazione che crea i corsi, i profili degl altri utenti e ne gestisce le info uniche, come l'ID |

<a name="sp1.3"></a>

### 1.3 Lista e Funzionalità 
| ID | Nome | Descrizione |
| ----------- | ----------- | 
| 1 | Login | L'utente accede con credenziali valide al sistema |
| 2 | Consulta Lista Corsi | L'utente accede alla lista dei corsi a cui è iscritto |
| 3 | Lista Studenti iscritti al corso | L'utente può visualizzare l'elenco degli studenti iscritti al corso|
| 4 | Elenco Esami Attivi Corso | L'utente visualizza gli esami attivi per il corso selezionato |
| 5 | Aggiunta Esame Corso | L'utente aggiunge un appello al corso selezionato | 

<a name="p2"></a>

## Scenari

<a name="p2.1"></a>

### 2.1 Login

| ID: 1 | <u>Login<\u> |
| ----------- | ----------- | 
| Attore | Docente, Studente, Amministrazione |
| Tipo | Primario | 
| Precondizione | L'utente ha delle credenziali valide per il sistema |
| Scenario Principale | |
| 1. | L'utente inserisce la sua ID |
| 2. | L'utente inserisce la password |
| 3. | Il Sistema conferma che che le credenziali sono valide | 
| Postcondizione: | L'utente ha accesso al sistema; il sistema scarica o aggiorna un token di autenticazione |
| 2a | Scenario Alternativo: L'utente inserisce credenziali non valide |
| 1. | Il sistema segnala che non esiste un account per l'ID inserito |
| 2. | Il sistema suggerisce di contattare l'Amministrazione per la creazione di un account |
| 3. | Il sistema ritorna al punto 1 principale |
| 2b | Scenario Alternativo: L'utente inserisce la password non corretta < 3 volte |
| 1. | Il sistema notifica che la password non è valida e invita a digitarla di nuovo |
| 2. | Il sistema incrementa il counter dei fallimenti |
| 3. | Il sistema torna al punto 2 principale |
| 2c | Scenario Alternativo: L'utente inserisce la password non valide per la terza volta |
| 1. | Il sistema notifica che la password è errata per la terza volta |
| 2. | Il sistema blocca l'account e invia una mail di sblocco all'utente |
| 3. | Il sistema invita l'utente ad aggiornare la password dalla mail |

<a name="p2.2"></a>

### 2.2 Consulta Lista Corsi

| ID: 2 | Consulta Lista Corsi |
| ----------- | ----------- | 
| Attore | Docente (Principale), Studente (Principale) |
| Tipo | Primario |
| Precondizione | L'utente ha un'autenticazione valida; l'utente è autorizzato ad accedere ai corsi |
| Scenario Principale | |
| 1. | L'Utente seleziona l'anno scolastico |
| 2. | Il Sistema riporta i corsi di quell'anno per cui il docente è registrato |
| 3. | L'Utente clicca sul corso che vuole esaminare |
| 4. | Il sistema mostra le informazioni identificative del corso |
| Postcondizione | L'Utente ha accesso alle informazioni del corso specificato |

<a name="p2.3"></a>

### 2.3 Lista Studenti iscritti al corso

| ID: 3 | Lista Studenti iscritti al corso |
| ----------- | ----------- | 
| Attore | Docente (Principale), Amministrazione (Principale) |
| Tipo | Primario | 
| Precondizione | Autenticazione valida; Il Docente insegna il corso dell'esame |
| Scenario Principale | |
| 1. | Il Docente seleziona il corso |
| 2. | Il Docente sceglie l'opzione "Mostra Studenti Iscritti" |
| 3. | Il Sistema fornisce l'elenco degli studenti iscritti al corso |
| Postcondizione: | Il docente ha accesso alla lista degli studenti iscritti ad un corso |


<a name="p2.4"></a>

### 2.4 Elenco Esami Attivi Corso

| ID: 4 | Elenco Esami Attivi Corso |
| ----------- | ----------- | 
| Attore | Docente (Principale) |
| Tipo | Primario | 
| Precondizione | |
| Scenario Principale | Autenticazione valida; Il Docente insegna il corso dell'esame |
| 1. | Il Docente selezione il corso |
| 2. | Il Docente clicca su opzione "Lista Esami Corso" |
| 3. | Il Sistema mostra la lista degli esami del corso. |
| Postcondizione: | Il Docente visualizza la lista degli esami attivi |

<a name="p2.5"></a>

### 2.5 Aggiunta Esame Corso

| ID: 5 | Aggiunta Esame Corso |
| ----------- | ----------- | 
| Attore | Docente (Principale) |
| Tipo | Primario | 
| Precondizione | Autenticazione valida; Il Docente insegna il corso dell'esame |
| Scenario Principale | |
| 1. | L'utente visualizza la lista esami del corso |
| 2. | L'utense sceglie l'opzione "Aggiungi Esame" |
| 3. | L'utente inserisce la data/le date dell'appello |
| 4. | L'utente salva le informazioni |
| 5. | Il Sistema notifica la creazione dell'appello |
| 6. | Il Sistema invia una mail a tutti gli iscritti al corso |
| Postcondizione: | L'esame per il corso è stato creato |


<a name="p2.6"></a>

### 2.6

<a name="p2.7"></a>

### 2.7

<a name="p2.8"></a>

### 2.8

<a name="p2.9"></a>

### 2.9

<a name="p2.10"></a>

### 2.10

<a name="p2.11"></a>

### 2.11

<a name="p2.12"></a>

### 2.12

<a name="p2.13"></a>

### 2.13

<a name="p2.14"></a>

### 2.14

<a name="p2.15"></a>

### 2.15

<a name="p2.16"></a>

### 2.16

<a name="p2.16"></a>

### 2.16

<a name="p2.17"></a>

### 2.17