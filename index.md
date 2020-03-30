# Cos'è FBforchildren?
In tutta Italia e non solo, l'associazione nasce per aiutare tutti i bambini, dalla loro nascita alla loro adolescenza, che non hanno possibilità di avere il necessario per la loro crescita. Da circa 6 anni a questa parte FBforchildren ha creato e messo a disposizione uno strumento semplice come un gruppo facebook (vedi link:https://www.facebook.com/groups/1511357489095363/), di oltre 15mila utenti, dove chiunque disponga di vestiti, giocattoli, accessori scolastici ed altro utile alla crescita di questi bambini riesce a mettersi in contatto con chi ne ha bisogno per offrirglieli in dono.

### FBforchildren vuole usare più tecnologia per aiutare più persone
Il gruppo Facebook, nonostante il numero elevato e in costante crescita di utenti, è uno strumento che presenta dei limiti. FBforchildren vuole creare una piattaforma propria all'interno della quale continuerà a fare quello che sta facendo, ma con la possibilità di utilizzare più tecnologie, che in una piattaforma propria possono essere ideate e inserite (geolocalizzazione, ricerca degli oggetti più precisa ecc..), con lo scopo di raggiungere più persone che hanno bisogno di questi oggetti pronti per essere donati.


### Che app costruieremo e in che modalità
Si vuole creare un'app nativa con Apache Cordova (vedi link: https://cordova.apache.org/) con i linguaggi di programmazione web, tra cui php o python (lato server), javascript (lato client), html e css per l'interfaccia grafica. In questo modo, con un solo progetto avremo creato un'app che giri su Android, iOS, Windows e anche il sito internet. E' importante dire ai programmatori che <strong>per utilizzare Apache Cordova con lo scopo di creare un'app nativa per dispositvi mobile si deve creare come qualsiasi sito internet applicativo ricordando le richieste al server vanno fatte con chiamate ajax (si veda il link: https://www.html.it/pag/44428/scambio-dei-dati-online-e-connettivita/)</strong>.

# Costruiamo insieme l'app FBforchildren!
Abbiamo suddiviso il lavoro in 4 categorie:
- Utenti
- Sessione dell'utente che ha effettuato l'accesso
- Pubblicazione oggetti da donare
- Interfaccia amminastrore e moderatori

### Utenti
Gli utenti si dividono tra utente semplice, moderatore e amministratore. La registrazione è uguale per tutti, gli eventuali ruoli di moderatore o amministratore verranno affidati in un secondo momento dagli amministratori esistenti (per questo si legga la categoria Interfaccia amministratore e moderatori).
Nella fase di registrazione i campi che devono essere inseriti sono:
- Nome 
- Cognome
- Città di residenza (con provincia e CAP)
- Password per accedere
- Social network o numero di telefono in cui si vuole essere ricontattati per donare gli oggetti. (Obbligatorio almeno uno)
- Il database genererà in automatico un id utente, questo sarà importante per gestire le sessioni (importante verificare che sia univoco cioè che non ne esistano altri utenti registrati con lo stesso id utente)

!!!ATTENZIONE dilemma da risolvere insieme (?)
La registrazione deve essere confermata (ad esempio con l'inserimento di un codice che si riceve per SMS, o il click di una mail che si riceve all'indirizzo specificato), ma abbiamo deciso di discutere insieme a voi collaboratori di questo punto.

Una volta effettuata la registrazione l'utente potrà accedere all'app inserendo i campi: 
- Email, se si è deciso di confermare la registrazione con questo, o numero di telefono se si è deciso di farlo con il codice inviato con SMS
- Password

### Sessione dell'utente che ha effettuato l'accesso
Una volta effettuato l'accesso l'utente vedrà in una tendina (tipo quella facebook in qui con uno scroll si vedono i post che i nostri amici pubblicano) gli oggetti che gli utenti intendono donare nella città che lui ha indicato come città di residenza durante la registrazione (campo che si deve avere la possibilità di cambiare in qualsiasi momento) ed eventualmente se lo desidera, cliccando su uno specifico tasto, potrà vedere anche quelli di tutta la provincia e/o della regione della città indicata in fase di registrazione o eventualmente modificata in un secondo momento.

Abbiamo quindi detto che nello scroll di questa tendina vi saranno i post degli oggetti che si intendono donare, questi post devono contenere le seguenti informazioni dell'utente che vuole donare e degli oggetti che si intendono donare:
- Nome e cognome 
- Foto e descrizione degli oggetti (per questo si vede la categoria Publicazione oggetti da donare)
- Città in cui si vuole donare
- Recapiti social in cui ricontattarlo (ovviamente quelli che l'utente che intende donare ha specificato durante la sua registrazione)

Nella stessa interfaccia in qui si trova la tendina con tutti gli oggetti da donare vi sarà disponibile un campo cerca, utile a ricercare in modo più dettagliato l'oggetto di cui si ha bisogno. Il campo cerca deve richiedere le seguenti informazioni per effettuare una ricerca più dettagliata:
- Oggetto (cosa si sta cercando)
- categoria oggetto (esempio vestiti, giocattoli ecc..)
- Se si vuole cercare solo in città, in tutta la provincia o la regione.

Nella stessa interfaccia, oltre al campo cerca, vi sarà la possibilità di switchare per scegliere se nella tendina devono essere presenti solo oggetti disponibili in città, in tutta la provincia o in tutta la regione e inoltre un tasto che una volta cliccato permetterà di pubblicare oggetti che si vogliono donare(si veda la categoria pubblicazione oggetti da donare).

### Pubblicazione oggetti da donare
Quando l'utente clicca sul tasto che gli permette di accedere a questa categoria gli verranno chieste le seguenti informazioni:
- Categoria oggetto (esempio vestiti, giocattoli ecc..)
- Oggetto che si vuole donare (un titolo ad esempio)
- Descrizione oggetti 
- Foto degli oggetti (non obbligatorio, ma utile, per questi motivi dobbiamo dare la possiblità di scattare una foto in questa fase)
- Città in cui si vuole donare (che per default, se non viene inserita in questo campo, prenderà quella indicata in fase di registrazione dall'utente)

Una volta inserite tutte le informazioni utili e inviate il post verrà subito pubblicato.

### Interfaccia amminastrore e moderatori
L'interfaccia 



```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/fbforchildren/FBforchildrenAPP/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
