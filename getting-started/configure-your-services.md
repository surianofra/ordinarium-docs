---
description: >-
  Your restaurant services represent the various order types you accept. View
  our video for an in-depth explanation of all the settings available.
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

## Custom Service Hours

Each service can have its own independent operating hours. Setting custom operating hours for a particular service will override the operating hours set for your store location.

## Estimated Wait Times & Auto Statuses

To help you better manage your orders and customer expectations, we provide a streamlined way to calculate order wait times and automatically update statuses. There are 6 order statuses:

* Un-confirmed
* Confirmed
* Ready
* On Route (delivery only)
* Complete
* Cancelled

Both estimated wait times and automated status updates are connected to the same timing settings. This is so that your status updates and wait times are in sync with each other. This avoids any customer confusion. These timing settings are:

| Setting (minutes)                  | From Status | To Status |
| ---------------------------------- | ----------- | --------- |
| Time till confirm                  | Unconfirmed | Confirmed |
| Time till ready                    | Confirmed   | Ready     |
| Time till on route (delivery only) | Ready       | On Route  |
| Time till complete                 | Ready       | Complete  |

{% hint style="info" %}
* Time till confirm is the time between when an order is placed to when it's confirmed. Setting time till confirm to "0" will result in instant order confirmation. You will need to also enable auto status for the confirmed status.
* Time till ready is the time it takes you to prepare an order after it's confirmed
* The time till on route status is effectively the time between when an order is prepared to when it is taken by the delivery driver.
* Time till complete is useful for automatically marking orders as complete
{% endhint %}

### Estimated Wait Times

As stated, customer wait times are calculated using the above timing settings.

#### How estimated wait time are calculated for pickup or dine-in orders

For pickup and dine-in orders, the estimated wait time is calculating buy adding the **time till confirm** with the **time till ready** values. So for example, if your **time till confirm** was 5 and your **time till ready** was 20. The customer would get an estimated wait time of 20 + 5 = 25 minutes.

If you have not added a value for time till confirm or time till ready, the estimated wait time would not be calculated.

#### How estimated wait time is calculate for delivery orders

For deliveries, the wait time is calculating by adding the **time till confirm** + **time till ready** + **time till on route** together. Then the **driving time** is added onto that. The driving time is determined using an external service that takes into account traffic data. This provides the customer with an extremely accurate wait time for their order to be delivered. Assuming

If you have not added a value for time till confirm or time till ready or time till on route, the delivery time would not be calculated.

### Automated Statuses

Automated statuses change an order's status after a set period of time has passed. This will allow you to do things such as:

* Automatically confirm new orders
* Mark orders as ready after a period of time
* Mark orders as complete after a period of time

This is very helpful if you know your business timings well and don't want to manually be updating order statuses. Auto status updates can also be enabled or disabled on a per status basis. This way you can provide estimated wait times without auto-updating statuses. Or you can just instantly confirm orders and handle the rest manually.

For automated status updates to work, you will need to enable it for a particular status and ensure the timing settings are added to that particular status.

#### How automated statuses work

Status updates are dependent on your timing settings, the type of order and the order due time. It's best explained through a series of examples.

For the examples, we will assume our timing settings are as follows

* Time till confirm - 10 minutes
* Time till ready - 10 minutes
* Time till on route - 10 minutes
* Time till complete - 60 minutes

#### Pickup and dine-in examples

If a customer places an order at 7:00pm for pickup or dine in which is due immediately

| Time   | Action                                                                                                                                     |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 7:00pm | Order has been placed, status unconfirmed                                                                                                  |
| 7:10pm | Status updated to confirmed because time till confirm is 10 minutes                                                                        |
| 7:20pm | Status updated to ready because time till ready is 10 minutes. This would also be the estimated order ready time as shown to the customer. |
| 8:20pm | Status updated to complete because time till complete is 60 minutes                                                                        |

In the event that you added an extra 10 minutes onto the customers estimated order ready time, it will play out as follows:

| Time   | Action                                                                                                                  |
| ------ | ----------------------------------------------------------------------------------------------------------------------- |
| 7:00pm | Order has been placed, status unconfirmed, you add 10 minutes to estimated ready time                                   |
| 7:10pm | Status updated to confirmed because time till confirm is 10 minutes                                                     |
| 7:30pm | Status updated to ready because the old ready time was 7:20pm, since you added an extra 10 minutes, that becomes 7:30pm |
| 8:30pm | Status updated to complete because time till complete is 60 minutes                                                     |

If we are unable to calculate an estimated ready time for the order, for example if the time till confirm was missing, it would play out as follows

| Time   | Action                                                              |
| ------ | ------------------------------------------------------------------- |
| 7:00pm | Order has been placed, status unconfirmed                           |
| 7:05pm | You manually update the order status to confirmed                   |
| 7:15pm | Status updated to ready, because the time till ready is 10 minutes  |
| 8:15pm | Status updated to complete because time till complete is 60 minutes |

If a customer places an order at 6:00pm for pickup or dine in which is due at 7:00pm, the following would occur

| Time   | Action                                                                             |
| ------ | ---------------------------------------------------------------------------------- |
| 6:00pm | Order has been placed, status unconfirmed                                          |
| 6:10pm | Status updated to confirmed because time till confirm is 10 minutes                |
| 7:00pm | Status updated to ready, because this is when the customer scheduled the order for |
| 8:00pm | Status updated to complete because time till complete is 60 minutes                |

#### Delivery examples

For the delivery examples, we will assume the driving time between your store and the delivery address is calculated as 10 minutes.

If a customer places a delivery order at 7:00pm which is due immediately

| Time   | Action                                                                                                                         |
| ------ | ------------------------------------------------------------------------------------------------------------------------------ |
| 7:00pm | Order has been placed, status unconfirmed                                                                                      |
| 7:10pm | Status updated to confirmed because time till confirm is 10 minutes                                                            |
| 7:20pm | Status updated to ready because time till ready is 10 minutes                                                                  |
| 7:30pm | Status updated to on route because time till on route is 10 minutes. This would also be shown to you as the driver pickup time |
| 7:40pm | Order will have been delivered to customer since the driving time is 10 minutes                                                |
| 8:40pm | Order marked as completed because time till complete is 60 minutes                                                             |

If we were unable to calculate the estimated delivery time and driver pickup time, say if the time till on route was missing, the following would occur

| Time   | Action                                                                          |
| ------ | ------------------------------------------------------------------------------- |
| 7:00pm | Order has been placed, status unconfirmed                                       |
| 7:10pm | Status updated to confirmed because time till confirm is 10 minutes             |
| 7:20pm | Status updated to ready because time till ready is 10 minutes                   |
| 7:40pm | You manually mark the order an on route for delivery                            |
| 7:50pm | Order will have been delivered to customer since the driving time is 10 minutes |
| 8:50pm | Order marked as completed because time till complete is 60 minutes              |

If a customer places a delivery order at 6:00pm which is due at 7:00pm, the following would occur

| Time   | Action                                                                                                                                                                                                  |
| ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 6:00pm | Order has been placed, status unconfirmed                                                                                                                                                               |
| 6:10pm | Status updated to confirmed because time till confirm is 10 minutes                                                                                                                                     |
| 6:40pm | Status updated to ready because delivery time is 10 minutes and time till on route is 10 minutes, which means that the order must be ready by this time if it is going to reach your customer at 7:00pm |
| 6:50pm | Status updated to on route because the delivery time is 10 minutes, so it has to leave your store at this time. This is also the estimated driver pickup time.                                          |
| 7:00pm | Order will have been delivered to customer                                                                                                                                                              |
| 8:00pm | Order marked as completed because time till complete is 60 minutes                                                                                                                                      |

If a delivery order is scheduled for a later time but the estimated delivery time could not be calculated, then the ready and on route status will not update automatically.

{% hint style="info" %}
If ever in doubt about how the auto status timings will work for your scenario, just think about how it would logically work in a way that makes sense to your customer and you. That is how we have designed it to work.
{% endhint %}
