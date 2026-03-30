# Verifica pratica: Git, Shell, Docker

## Obiettivo

In questa prova dovrai:

1. clonare il repository;
2. creare un tuo branch personale;
3. creare una tua cartella di lavoro;
4. realizzare un semplice script Python;
5. creare un `Dockerfile` per eseguire lo script in un container;
6. *(opzionale) scrivere uno script shell per automatizzare build ed esecuzione;*
7. *(opzionale) generare un file di output;*
8. salvare ed inoltrare il lavoro con `git`
---

## Requisiti

Prima di iniziare assicurati di avere disponibili:

- Git
- Docker
- Python 3
- una connessione Internet attiva (per scaricare l'immagine base Docker, se necessario)

---
---


## Attività da svolgere

### 1. Clona il repository

Clona questo repository sul tuo computer.

Comando atteso:
```bash
git clone <URL_DEL_REPOSITORY>
```


### 2. Crea il tuo branch personale

Dopo essere entrato nel repository, crea un branch con il tuo nome **e spostati** su quel branch.

Esempio comando:
```bash
git checkout -b mario-rossi
```

### 3. Crea la tua cartella personale

All'interno del repository, crea una nuova cartella usando il tuo nome e cognome (tutto minuscolo e separato da un trattino).
Subito dopo, **entra in questa cartella.**


Ora la tua area di lavoro dovrebbe presentarsi in questo modo:

```bash
esercitazione-ITS/
├── README.md           # Il file con queste istruzioni (già presente)
└── mario-rossi/        # La cartella che hai appena creato (ORA SEI QUI)
    ├── ...             
    ├── ...             # (qui dentro creerai tutti i tuoi file)
    └── ...            
```


### 4. Crea il file Python

All'interno della tua cartella personale, crea un file chiamato:

```
app.py
```

Questo programma deve stampare a schermo tre informazioni:

- il tuo nome e cognome;

- la data e l'ora correnti;

- un numero casuale compreso tra 1 e 100.

Un esempio di output è il seguente:
```text
Studente: Mario Rossi
Data e ora: 2026-03-31 12:30:15
Numero casuale: 42
```

⚠️ Attenzione: Il file app.py deve trovarsi dentro la tua cartella personale, non nella cartella principale del repository.

### 5. Crea il Dockerfile

Rimanendo sempre all'interno della tua cartella personale, crea un file chiamato esattamente:

```text
Dockerfile
```

Questo file deve contenere le istruzioni per "impacchettare" lo script Python all'interno di un container.
I passi da implementare saranno quindi:
1) Scegliere un'immagine di base
2) Impostare l'ambiente
3) Copiare il codice
4) Definire il comando di avvio (**CMD**)


### 6. *Crea lo script shell (opzionale)*

Rimanendo all'interno della tua cartella personale, crea un file chiamato:

```text
run.sh
```

Questo script Bash deve automatizzare la creazione e l'esecuzione del tuo container Docker.
I comandi necessari saranno quindi:
- Indicare la shell da utilizzare (*shebang*)
- Costruire l'immagine Docker (**build**)
- Eseguire il container e salvare l'output (**run**)

    ⚠️ Attenzione: non limitarti a stampare a video, ma usa l'operatore di reindirizzamento (**>**) per salvare l'output del container in un file chiamato esattamente **risultato.txt**.


### 7. *Esegui lo script shell per test (opzionale)*

Fai girare lo script Bash che hai creato

1) Rendi lo script eseguibile
2) Esegui lo script e verifica il file **risultato.txt**


### 8. Controlla i file creati

Prima di concludere, verifica di aver creato correttamente tutti i file richiesti nella tua cartella personale.

Dentro la tua cartella devono essere presenti almeno questi file:

```bash
app.py
Dockerfile
run.sh          # opzionale
risultato.txt   # opzionale
```


### 9. Salva e inoltra il lavoro con Git
Quando hai terminato il lavoro, salva le modifiche e inviale sul repository remoto usando Git.

**Rimanendo sul branch personale:**
1) Esegui un commit locale
2) Invia sul repository remoto

    Suggerimento: 
    ```bash
    cd ..
    
    git push -u origin nome-cognome
    ```
    per rimanere sul branch personale!