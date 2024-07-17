---
description: >-
  I servizi locale rappresentano i vari tipi di ordine che accetti. Guarda il
  video per una spiegazione approfondita di tutte le impostazioni disponibili.
---

# Configurare i servizi

{% embed url="https://youtu.be/EUW9nZVAE68" %}
Services video tutorial
{% endembed %}

Attualmente sono disponibili 4 servizi che sono:

* Pickup - ordini che vengono ritirati nel locale dai clienti per essere portati via
* Delivery - ordini che vengono consegnati all'indirizzo del cliente
* Dine-in - ordini effettuati dai clienti all'interno del locale, anche direttamente dal tavolo
* Table booking - una prenotazione effettuata per una data e un orario successivi

## Come configurare i servizi

1. Visita la dashboard del locale e vai alla pagina delle impostazioni.
2. Seleziona la scheda "Servizi" e modifica le impostazioni come si preferisce.

## Abilitare e disabilitare dei servizi

È possibile attivare o disattivare i servizi a seconda delle necessità. Vai alle impostazioni del servizio desiderato e premi l'interruttore "Enabled" per attivarlo o disattivarlo.

{% hint style="info" %}
È necessario che sia abilitato almeno un servizio
{% endhint %}

## Note nei servizio

È possibile aggiungere note personalizzate per ogni servizio, che verranno mostrate al cliente una volta selezionato. Utile se hai bisogno di trasmettere un messaggio importante al cliente.

## Tempi dell'ordine

Un cliente può effettuare un ordine con scadenza immediata solo se il locale è aperto. Gli ordini per una data successiva devono essere programmati entro gli orari di apertura del locale. Pertanto, le tempistiche degli ordini sono controllate principalmente dagli orari di apertura del negozio. Ogni servizio ha poi le proprie impostazioni separate per la tempistica degli ordini, che consentono un controllo più approfondito.

### Abilitare e disabilitare i tempi di ordinazione

Nella scheda "Order Timings" delle impostazioni del servizio, è possibile attivare e disattivare gli ordini immediati e quelli programmati.

### Scostamento primo ordine

È il periodo di tempo che intercorre tra l'apertura del locale e l'accettazione del primo ordine. Ad esempio, se l'offset del primo ordine è impostato su 30 minuti e il locale apre alle 9:00, il primo ordine può essere inserito o programmato alle 9:30.

### Scostamento ultimo ordine

È il periodo di tempo che intercorre tra la chiusura del locale e l'accettazione dell'ultimo ordine. Ad esempio, se l'offset dell'ultimo ordine è impostato su 30 minuti e il locale chiude alle 21:00, l'ultimo ordine potrà essere inserito o programmato alle 20:30.

### Scostamento Ordine

La normale compensazione degli ordini si applica solo agli ordini programmati in un momento successivo. Si tratta del periodo a partire dal quale è possibile effettuare un ordine programmato. Ad esempio, serve per evitare che i clienti programmino un ordine nei prossimi 10 minuti, invece di chiedere che venga effettuato il prima possibile.

Quindi, ad esempio, se lo scostamento degli ordini è di 30 minuti e l'ora corrente è 18:00, il momento successivo in cui un cliente può programmare un ordine è alle 19:00. Se lo desidera prima delle 19:00, il cliente può programmarlo prima delle 19:00. Se lo desidera prima delle 19:00, può comunque ordinare al più presto. Se lo scostamento dell'ordine è di 15 minuti, il cliente può ordinare per le 18:30.

L'offset dell'ordine funge anche da punto di interruzione per dare il tempo di soddisfare la pianificazione dell'ordine. Ad esempio, se sono le 18:00 e l'offset dell'ordine è di 30 minuti. Se il cliente ha programmato un ordine per le 19:00, deve effettuare l'ordine prima delle 18:30. Questo per darti 30 minuti per rispettare l'orario previsto.

Se il cliente impiega troppo tempo e l'orario supera le 18:30, riceverà una notifica che gli comunicherà che l'ordine è stato modificato per essere consegnato al più presto, invece che alle 19:00, orario previsto.

## Orari di servizio personalizzati

Ogni servizio può avere un proprio orario indipendente. L'impostazione di orari personalizzati per un particolare servizio sovrascrive gli orari generici per quel servizio specifico..

## Tempi di attesa stimati e stati automatici

Per aiutarti a gestire meglio gli ordini e le aspettative dei clienti, ti forniamo un metodo semplificato per calcolare i tempi di attesa degli ordini e aggiornare automaticamente gli stati. Esistono 6 stati dell'ordine:

* Non confermato
* Confermato
* Pronto
* In arrivo (solo per delivery)
* Completato
* Cancellato

Sia i tempi di attesa stimati che gli aggiornamenti di stato automatici sono collegati alle stesse impostazioni di temporizzazione. In questo modo gli aggiornamenti di stato e i tempi di attesa sono sincronizzati tra loro. In questo modo si evita di confondere i clienti. Le impostazioni di temporizzazione sono:

| Impostazione (minuti)  | Da Stato       | A Stato     |
| ---------------------- | -------------- | ----------- |
| Tempo per la conferma  | Non confermato | Confermato  |
| Tempo di preparazione  | Confermato     | Pronto      |
| Tempo di partenza      | Pronto         | In consegna |
| Tempo di completamento | Pronto         | Completo    |

{% hint style="info" %}
* Il tempo di conferma è il tempo che intercorre tra l'invio di un ordine e la sua conferma. Impostando il tempo di conferma a "0", la conferma dell'ordine sarà immediata. È necessario attivare anche lo stato automatico per la conferma.
* Il tempo di preparazione è il tempo necessario per preparare un ordine dopo la sua conferma.
* Il tempo di partenza è effettivamente il tempo che intercorre tra la preparazione di un ordine e il momento in cui viene preso in consegna dal rider.
* Il tempo di completamento è utile per contrassegnare automaticamente gli ordini come completi, rispettando i tempi indicati nelle altre fasi.
{% endhint %}

### Tempi di attesa stimati

Come detto, i tempi di attesa dei clienti sono calcolati utilizzando le impostazioni di temporizzazione di cui sopra.

#### Come vengono calcolati i tempi di attesa stimati per gli ordini da asporto o al tavolo

Per gli ordini da asporto e al tavolo, il tempo di attesa stimato si calcola sommando i valori di tempo di conferma e di preparazione. Ad esempio, se il tempo di attesa per la conferma è di 5 minuti e il tempo di attesa per la preparazione è di 20 minuti, il cliente otterrebbe un tempo di attesa stimato di 20 + 5 = 25 minuti.

Se non è stato aggiunto un valore per il tempo di conferma o il tempo di preparazione, il tempo di attesa stimato non verrà calcolato.

#### Come viene calcolato il tempo di attesa stimato per gli ordini delivery

Per le consegne, il tempo di attesa si calcola sommando il tempo di conferma + il tempo di preparazione + il tempo di partenza. Poi si aggiunge il tempo di guida. Il tempo di guida viene determinato utilizzando un servizio esterno che tiene conto dei dati sul traffico. In questo modo il cliente ottiene un tempo di attesa estremamente preciso per la consegna del suo ordine.

Se non è stato aggiunto un valore per il tempo di conferma, il tempo di preparazione o il tempo di viaggio, il tempo di consegna non verrà calcolato.

### Stati automatici

Gli stati automatici modificano lo stato di un ordine dopo un determinato periodo di tempo. Questo vi permetterà di fare cose come:

* Confermare automaticamente i nuovi ordini
* Contrassegnare gli ordini come pronti dopo un certo periodo di tempo
* Contrassegnare gli ordini come completi dopo un certo periodo di tempo

Questo è molto utile se si conoscono bene i tempi della propria attività e non si vuole aggiornare manualmente lo stato degli ordini. Gli aggiornamenti automatici dello stato possono anche essere attivati o disattivati in base allo stato. In questo modo è possibile fornire tempi di attesa stimati senza aggiornare automaticamente gli stati. Oppure si può semplicemente confermare istantaneamente gli ordini e gestire il resto manualmente.

Affinché gli aggiornamenti di stato automatici funzionino, è necessario abilitarli per un particolare stato e assicurarsi che le impostazioni di temporizzazione siano aggiunte a quel particolare stato.

#### Come funzionano gli stati automatici

Gli aggiornamenti di stato dipendono dalle impostazioni di temporizzazione, dal tipo di ordine e dalla scadenza dell'ordine. Il modo migliore per spiegarlo è con una serie di esempi.

Per i prossimi esempi, assumiamo che le impostazioni di temporizzazione siano le seguenti

* Tempo di conferma - 10 minuti
* Tempo di preparazione - 10 minuti
* Tempo di partenza - 10 minuti
* Tempo di completamento - 60 minuti

#### Esempi di ritiro e ordini al tavolo

Se un cliente effettua un ordine alle 19:00 per il ritiro o la cena, la richiesta è immediata.

| Ora   | Azione                                                                                                                                                              |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 19:00 | L'ordine è stato effettuato, lo stato non confermato.                                                                                                               |
| 19:10 | Lo stato viene aggiornato a confermato perché il tempo di conferma è di 10 minuti.                                                                                  |
| 19:20 | Lo stato viene aggiornato a pronto perché il tempo di attesa è di 10 minuti. Questo sarebbe anche il tempo stimato di preparazione dell'ordine mostrato al cliente. |
| 20:20 | Lo stato viene aggiornato a completo perché il tempo di completamento è di 60 minuti.                                                                               |

Se si aggiungono 10 minuti in più al tempo stimato di preparazione dell'ordine del cliente, il risultato sarà il seguente:

| Ora   | Azione                                                                                                                                                 |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 19:00 | L'ordine è stato effettuato, lo stato è non confermato, si aggiungono 10 minuti al tempo di preparazione stimato.                                      |
| 19:10 | Lo stato viene aggiornato a confermato perché il tempo di conferma è di 10 minuti.                                                                     |
| 19:30 | Lo stato viene aggiornato a pronto perché il vecchio orario di pronto era le 19:20, ma dato che sono stati aggiunti altri 10 minuti, diventa le 19:30. |
| 20:30 | Lo stato viene aggiornato a completo perché il tempo di completamento è di 60 minuti.                                                                  |

Se non possiamo calcolare un tempo stimato di preparazione per l'ordine, ad esempio se manca il tempo di conferma, la situazione si presenterà come segue:

| Ora   | Azione                                                                                |
| ----- | ------------------------------------------------------------------------------------- |
| 19:00 | L'ordine è stato effettuato, lo stato è non confermato.                               |
| 19:05 | Aggiorni manualmente lo stato dell'ordine a confermato.                               |
| 19:15 | Stato aggiornato a pronto, perché il tempo di preparazione è di 10 minuti.            |
| 20:15 | Lo stato viene aggiornato a completo perché il tempo di completamento è di 60 minuti. |

Se un cliente effettua un ordine alle 18:00 per il ritiro o ordine al tavolo, che deve essere consegnato alle 19:00, si verificherà quanto segue:

| Ora   | Azione                                                                                            |
| ----- | ------------------------------------------------------------------------------------------------- |
| 18:00 | L'ordine è stato effettuato, lo stato è non confermato.                                           |
| 18:10 | Lo stato viene aggiornato a confermato perché il tempo di conferma è di 10 minuti.                |
| 19:00 | Lo stato viene aggiornato a pronto, perché il cliente ha programmato l'ordine per questo momento. |
| 20:00 | Lo stato viene aggiornato a completo perché il tempo di completamento è di 60 minuti.             |

#### Esempi di delivery

Per gli esempi di delivery, assumiamo che il tempo di guida tra il vostro locale e l'indirizzo di consegna sia di 10 minuti.

Se un cliente effettua un ordine di consegna alle 19:00 che deve essere evaso immediatamente

| Ora   | Azione                                                                                                                                                                          |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 19:00 | L'ordine è stato effettuato, lo stato è non confermato.                                                                                                                         |
| 19:10 | Lo stato viene aggiornato a confermato perché il tempo di conferma è di 10 minuti.                                                                                              |
| 19:20 | Stato aggiornato a pronto, perché il tempo di preparazione è di 10 minuti.                                                                                                      |
| 19:30 | Lo stato viene aggiornato a “In viaggio” perché il tempo mancante al raggiungimento del percorso è di 10 minuti. Questo viene mostrato anche come orario di prelievo del rider. |
| 19:40 | L'ordine viene consegnato al cliente in quanto il tempo di percorrenza è di 10 minuti.                                                                                          |
| 20:40 | L'ordine viene contrassegnato come completato perché il tempo di completamento è di 60 minuti.                                                                                  |

Se non fossimo in grado di calcolare l'orario di consegna stimato e l'orario di ritiro del rider, ad esempio se mancasse il tempo di percorrenza sul percorso, si verificherebbe quanto segue

| Tempo | Azione                                                                                         |
| ----- | ---------------------------------------------------------------------------------------------- |
| 19:00 | L'ordine è stato effettuato, lo stato è non confermato.                                        |
| 19:10 | Lo stato viene aggiornato a confermato perché il tempo di conferma è di 10 minuti.             |
| 19:20 | Stato aggiornato a pronto, perché il tempo di preparazione è di 10 minuti.                     |
| 19:40 | Contrassegni manualmente l'ordine come in fase di consegna.                                    |
| 19:50 | L'ordine viene consegnato al cliente in quanto il tempo di percorrenza è di 10 minuti.         |
| 20:50 | L'ordine viene contrassegnato come completato perché il tempo di completamento è di 60 minuti. |

Se un cliente effettua un ordine Delivery alle 18:00 con scadenza alle 19:00, si verificherà quanto segue

| Time  | Action                                                                                                                                                                                                                                  |
| ----- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 18:00 | L'ordine è stato effettuato, lo stato è non confermato.                                                                                                                                                                                 |
| 18:10 | Lo stato viene aggiornato a confermato perché il tempo di conferma è di 10 minuti.                                                                                                                                                      |
| 18:40 | Lo stato viene aggiornato a pronto perché il tempo di consegna è di 10 minuti e il tempo di attesa per la partenza è di 10 minuti, il che significa che l'ordine deve essere pronto a quest'ora se deve arrivare al cliente alle 19:00. |
| 18:50 | Lo stato viene aggiornato a “In viaggio” perché il tempo di consegna è di 10 minuti, quindi deve lasciare il locale a quest'ora. Questo è anche l'orario di ritiro stimato dal rider.                                                   |
| 19:00 | L'ordine è stato consegnato al cliente                                                                                                                                                                                                  |
| 20:00 | L'ordine viene contrassegnato come completato perché il tempo di completamento è di 60 minuti.                                                                                                                                          |

Se un ordine di consegna è programmato per un'ora successiva, ma non è stato possibile calcolare il tempo di consegna stimato, lo stato di pronto e in viaggio non verrà aggiornato automaticamente.

{% hint style="info" %}
In caso di dubbi sul funzionamento delle tempistiche dello stato automatico per il vostro scenario, pensate a come funzionerebbe logicamente in un modo che abbia senso per il vostro cliente e per voi. Questo è il modo in cui abbiamo progettato il funzionamento.
{% endhint %}

