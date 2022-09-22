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
|0.1| 22/09 | Seren, Federico, Tiziano | Update lista funzionalità e scenario |
|0.1| 22/09 | Federico Zunino | Creazione documento srs, update lista attori|

# Table of Contents

1. [User Case](#p1)
	1. [Diagramma](#sp1.1)
	2. [Attori](#sp1.2) 
	3. [Lista Funzionalità](#sp1.3)
2. [Scenari](#p2)
	1. [](#sp2.1)
	2. [](#sp2.2)

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
