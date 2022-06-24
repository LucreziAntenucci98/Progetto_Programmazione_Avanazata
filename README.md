# Progetto-Programmazione-Avanazata 

## Team

**• Antenucci Lucrezia** \
**• Leli Samuele**

## Obiettivo del Progetto

L'obiettivo del progetto è stato quello di realizzare un servizio di back-end utilizzando dei framework specifici, che consenta la gestione delle aste online chiamate Aste Snap.
In particolare il sistema prevede la possibilità di:

**•Creazione di una nuova Asta** \
**•Visualizzare l'elenco delle asta, filtrando per stato (creata,aperta,rilancio,terminata)** \
**•Partecipazione ad un'astra mediante autenticazione bid-partecipant e deve essere aperta** \
**•Rilancio con ruolo bid-creator** \
**•Visualizzare l'elenco dei rilanci per un'asta alla quale si sta partecipando e si è nella fase di rilancio** \
**•Gestione del "wallet" degli utenti** \
**•Gestione dell'iscrizione** \
**•Gestione del caso in cui non si raggiunge il numero di partecipanti** \
**•Gestione del credito(somma dei costi di iscrizione + prezzo massimo asta), con eventuale rifiuto(bid-partecipant)** \
**•Visualizzazione del proprio credito residuo** \
**•Creazione di una rotta per ricaricare l'utente** \
**•Dopo essersi aggiudicati l'asta , viene scalato il credito** \
**•Visualizzazione dello storico delle aste (aggiudicate e non)** \
**•Visualizzare la spesa effettuata in un dato periodo temporale a seguito delle eventuali aggiudicazioni intercorse oltre che alle quote di iscrizioni effettivamente scalate** \
•**Fornire delle statistiche attraverso le quali in un dato intervallo temporale è necessario fornire i seguenti dettagli**: 

  * n° di aste completate con successo ;
  
  * n° aste terminate per non aver raggiunto il numero minimo di iscritti;
  
  * Media del rapporto tra numero di puntate effettuate e numero massimo di puntate effettuabili.


Ogni azione corrisponde a una differente richiesta HTTP (GET o POST) che deve essere, o meno, autenticata tramite token JWT.

## Strumenti Utilizzati 

* [VisualStudio Code](https://code.visualstudio.com/)
* [Docker](https://docs.docker.com/)
* [Postman](https://www.postman.com/)

## Librerie/Framework

**•	Node.JS** \
**•	Express** \
**•	Sequelize** \
**•	Postgres**


## Richieste
Tipo          | Rotta                         | Autenticazione JWT
------------- | ----------------------------- |--------------------
Post          | /creaAsta                     | si
Post          | /partecipaAsta                | si
Post          | /rilancia                     | si
Post          | /ricaricaUtente               | si
Get           | /verificaCreditoResidio       | si
Get           | /elencoRilanci                | si
Get           | /storicoAste                  | si
Get           | /speseEffettuate              | si
Get           | /stats                        | si
Get           | /VisualizzaAsteByStato        | no

## Uso delle rotte



## Progettazione - Diagrammi UML

Di seguito si riportano i diagrammi UML:

• Use Case Diagram 

![UMLcasid'uso](https://user-images.githubusercontent.com/86314085/175025430-2eadbd1a-3cf1-4ec9-8837-5baa92dced4d.png)




## Progettazione - Pattern

**• factory** : fa parte della famiglia dei pattern creazionali in quanto fornisce il modo migliore per creare un'eggetto. Creiamo oggetti senza passare per il client utilizzando un interfaccia comune.

![image](https://user-images.githubusercontent.com/86314085/175505855-c64a33b3-19c6-4fd0-abae-be3c4542f321.png)


**• observable** : permette di definire una dipendenza 1-N fra oggetti, in modo tale che se un oggetto cambia il suo stato interno, ogni oggetto che dipende da lui, viene notificato e aggiornato automaticamente. Serve per mantenere un alto livello di consistenza fra le classi correlate senza riprodurre un'accoppiamento elevato.

![image](https://user-images.githubusercontent.com/86314085/175506554-8ba9223d-22f4-4856-9b3a-308c430a3b6e.png)

Abbiamo un oggetto che viene osservato e tanti che osservano i cambiamenti di quest'ultimo

**• singleton** : Pattern creazionale. Coinvolge una singola classe che è responsabile della creazione dell'oggetto assicurandosi che  viene creato solo un singolo oggetto. FOrnisce un modo per accedere al suo unico oggetto, non ha necessità di creare un'istanza dell'oggetto della classe.

![image](https://user-images.githubusercontent.com/86314085/175507090-a971e7ba-51d4-4139-8206-9bf374b00e47.png)


**• builder** : pattern creazionale. Crea passo dopo passo l'oggetto finale ed è indipendente da altri oggetti.
![image](https://user-images.githubusercontent.com/86314085/175507520-a74675ea-503f-462b-9a61-822bdee15a4d.png)


**• middleware** : sono funzioni che prendono come argomento ad esempio request, responde..
Verifica inoltre se si può o meno autenticare o verificare, eseguire una rotta

## Avvio

**• Ambiente Docker installato sulla propria macchina**\
**• Clonare la seguente repository da terminale**\
```bash
git clone https://github.com/LucreziAntenucci98/Progetto_Programmazione_Avanzata
```
**•Eseguire il seguente comando:** (sostituire 'mysupersecretkey' con la chiave con la quale verranno generati i token JWT) 
```bash
$ echo 'KEY=mysupersecretkey' >> .env
```
**• Avviare Docker tramite**
```bash
docker-compose build
docker-compose up
```
**• Eseguire il servizio sulla porta 8080 tramite Postaman**


## Test







