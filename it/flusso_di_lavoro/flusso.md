# GITHUB MAPOD4D

Qui di seguito il flusso di lavoro utilizzato dalla community. Tale flusso è obbligatorio, non verranno accettate pull che non lo seguano!

## 1. Definizioni

- **Repository MAPOD4D:** repository salvato nel profilo _GitHub_ dell'organizzazione **MAPOD4D**.
- **Repository personale:** repository salvato nel proprio profilo _GitHub_.
- **Repository locale:** repository salvato nella memoria di massa (e.g. _Hard Disk_, _SSD_) del proprio PC.
- **Repo:** diminuitivo di repository.
- **Fork:** copia di un repository da un altro utente o organizzazione sul proprio profilo _GitHub_.

## 2. Prima di iniziare

- **creiamo un'area di lavoro:** se non si ha già un'area di lavoro, crearne una. Questa servirà a mettere tutte cartelle che si utilizzeranno per i lavori della community (Es.: _area_sviluppo_).

- **fork del repository MAPOD4D:** per effettuare il _fork_ un repository basta cliccare sul bottone **_Fork_** in alto a destra della pagina **Github** del _repository_. A questo punto nel vostro profilo _GitHub_ apparirà una copia del **_repository MAPOD4D_** che da ora chiameremo **_repository personale_**.

<!-- aggiungere per i grossi file -->

- **prendiamo il link del repository forkato:** Accedendo al vostro profilo _GitHub_ e successivamente al vostro **_repository personale_** potrete copiarne il link. Premendo il tasto verde "**Code**" apparirà un menú a tendina contenente il link.<!-- immagine tasto verde -->Il link apparirà nel seguente modo:

         https://github.com/[username]/[nome_repository].git

- **creiamo il repository localmente:**

        git clone --mirror https://github.com/[username]/[nome_repository].git

- **accediamo al repository:**

        cd [nome_repository]

- **settiamo i riferimenti dei repository remoti nel repository locale:** per settare i remoti si usano i seguenti comandi:

        git remote add mapod4d https://github.com/mapod4d/[nome_repository].git

  questi comandi serviranno a creare una connessione al repository principale soltanto per la _pull_ dei dati. **ATTENZIONE:** se sei amministratore, settare la push su NO PUSH (vedi riferimenti alla sezione [**Sei Amministratore?**](#sei-amministratore))

Una volta che il nostro ambiente di lavoro è pronto, possiamo iniziare a lavorare ai nostri task.

## 3. Gestione semplice di un task

1.  ritorniamo al master

        git checkout master

1.  scarichiamo possibili nuovi aggiornamenti dal repository principale

        git pull mapod4d master

    - risolviamo i conflitti

1.  puliamo la cache del repository

        git pull --prune

1.  portiamo le modifiche al repository locale

        git push origin master

1.  creiamo il branch dev (**se già creato, passare al punto 6**)

        git branch dev

1.  spostiamoci sul dev (**se non creato, passare al punto 5**)

        git checkout dev

1.  uniamo il master al dev

        git merge master

    - risolviamo eventuali conflitti
    - eseguiamo il task
    - facciamo add e commit ogni qualvolta raggiungiamo degli step di lavoro

          git add [nome_file + .estensione]

          git commit -m "[inserire titolo commit]"

    - finiamo di lavorare sul task

1.  portiamo le nostre modifiche nella repo personale

        git push -u origin dev

_Riprendere dal punto 1 finquanto la task non è terminata._

## 4. Hai finito la task?

1.  ritorniamo al master

        git checkout master

1.  scarichiamo possibili nuovi aggiornamenti dal repository principale

        git pull mapod4d master

    - risolviamo i conflitti

1.  uniamo il dev al master

        git merge dev

1.  portiamo le nostre modifiche nella repo personale

        git push origin master

    - risolviamo i conflitti

1.  andare alla sezione **Cosa succede ora?**

## 5. Cosa succede ora?

### Aprire una _Pull Request_

Bisogna accedere a GitHub ed effettuare la **_Pull Request_** cliccando su **_Contribute_** e cliccando sul tasto verde **Create Pull Request**. Nella nuova pagina, inserire il task come titolo e poi clicchiamo sul tasto **Create Pull Request**.

### Che farne ora del dev?

Prima di eliminare il branch su cui abbiamo lavorato, dobbiamo aspettare che ci venga data la conferma dell'avvenuta accettazione della **_Pull Request_**.

### Sei Amministratore?

- **settare i remoti nel repo locale:** per settare i remoti si usano i seguenti comandi:

        git remote add mapod4d https://github.com/mapod4d/[nome_repository].git
        git remote set-url --push mapod4d NOPUSH

  questi comandi serviranno a creare una connessione al repository principale soltanto per la _pull_ dei dati.
