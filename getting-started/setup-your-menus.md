---
description: >-
  Per accettare ordini online, è necessario impostare il proprio menu online. È
  possibile creare e gestire tutti i menu nella sezione "Menu" della dashboard
  del ristorante.
---

# Impostazione dei Menu

{% embed url="https://youtu.be/Nyyr2vwB1Io" %}
Video Tutorial Imostazione Menu
{% endembed %}

## Processo di impostazione

I menu sono organizzati in una struttura ad albero. I menu contengono categorie e le categorie contengono piatti. Il processo di configurazione generale è il seguente.

1. Crea un menù
2. Crea tutte le categorie del menu
3. Crea i piatti nelle categorie
4. Crea set di opzioni per aggiungere personalizzazione ai piatti
5. Creare tag di piatti per evidenziare gli attributi di particolari piatti e per segnalare gli allergeni.

{% hint style="info" %}
Probabilmente avrai bisogno di un solo menu. I menu multipli sono utili se alcune voci sono soggette a particolari restrizioni. Potrebbe essere necessario creare un menu "Colazione" o un menu "Consegna", a seconda delle esigenze.
{% endhint %}

## Esempio della struttura di un menù

```
- Menu: menu principale
-- Categoria: Pizze
---- Piatto: Prosciutto
---- Piatto: Margherita
---- Piatto: Vegetariana
-- Categoria: Sfiziosità
---- Piatto: Alette di Pollo
---- Piatto: Patatine Fritte
-- Categoria: Bevande
---- Piatto: Te freddo
---- Piatto: Coca Cola
---- Piatto: Acqua
```

## Menu

Questi rappresentano i menu reali. Molti locali hanno un solo menu principale sempre disponibile. Altri possono avere un menu per pranzo e cena o un menu per il solo ritiro. Per far funzionare le funzioni di ordini è necessario almeno un menu.

Si possono limitare o bloccare i menù in base ad alcune condizioni, come ad esempio il tipo di ordine (ritiro, consegna o al tavolo), la tempistica dell'ordine (subito, più tardi o solo su ordinazione). Possono anche essere limitati a determinati giorni e orari.

{% hint style="info" %}
Se si dispone di un solo menu, non è necessario imporre restrizioni. È possibile limitare il sistema a livello globale in base alle proprie regole aziendali e il menu funzionerà in base a tali regole. La restrizione di un menu a determinate condizioni è necessaria solo se si dispone di più menu.
{% endhint %}

## Categorie

Le categorie rappresentano una sottosezione di un menu e sono composte da piatti. Ad esempio, se avete un menu standard, le categorie potrebbero includere:

* Antipasti
* Primo
* Secondi
* Bevande
* Dolci

{% hint style="info" %}
In alcuni casi, potrebbe essere necessario creare un menu separato invece di utilizzare una categoria. Ad esempio, se hai molte categorie diverse di bevande, come liquori, vini, birre, bibite, ecc. si potrebbe creare un menu bevande separato per tutte queste categorie, invece di aggiungerle al menu degli alimenti.
{% endhint %}

## Piatti

I piatti rappresentano oggetti reali che possono essere acquistati. Esistono 2 tipi di piatti.

#### Piatti standard

Un piatto standard funziona come ci si aspetta. Lo si usa per creare oggetti come:

* Toast Classico
* Pizza Margherita
* Gelato alla vaniglia

**Ingredienti dei piatti**

I piatti standard possono contenere un elenco di ingredienti. Lo scopo è quello di consentire ai clienti di rimuovere facilmente alcuni ingredienti. Il cliente può rimuovere gli ingredienti indesiderati quando seleziona il piatto.

#### Piatti combinati

Le combinazioni sono un tipo speciale di piatti che contengono altri piatti. Consente di creare un elenco di scelte per i clienti che possono selezionare vari piatti standard. Ad esempio, è possibile creare:

* Scegli 3 pizze, 2 contorni e 2 bevande
* Scegli un hamburger, un contorno e una bevanda

Per farlo, è necessario aver creato alcuni piatti standard. Poi, quando si crea la combo, si possono creare 4 scelte, 3 scelte di pizza e una scelta di bevanda. È quindi possibile assegnare le scelte dei piatti alle pizze e alle bevande, in modo che i clienti possano scegliere.

{% hint style="info" %}
I piatti combinati non possono contenere direttamente set di opzioni o ingredienti. Invece, quando un cliente sceglie un piatto standard all'interno di un combo, se il piatto standard scelto ha dei set di opzioni assegnati, l'utente può personalizzarlo di conseguenza.
{% endhint %}

#### Disponibilità e stato dei piatti

Sono disponibili 3 stati per un piatto che sono:

* Nascosto - nasconde il piatto dal menu
* Disponibile - mostra il piatto dal menu e permette di ordinarlo
* Esaurito - impedisce l'ordine e mostra lo stato esaurito piatto

Nella dashboard di amministrazione, è possibile modificare lo stato di un piatto selezionando la casella di controllo a sinistra. Quindi selezionare lo stato desiderato dal menu a comparsa.

## Set di Opzioni

Tutte le **personalizzazioni dei piatti** vengono effettuate utilizzando i set di opzioni. I set di opzioni sono un insieme configurabile di opzioni che possono essere assegnate a qualsiasi numero di piatti. Con i set di opzioni è possibile creare requisiti quali:

* Selezionare il cornicione della pizza
* Selezionare una o più salse
* Selezionare almeno 4 condimenti

{% hint style="info" %}
Per imparare a creare un set di opzioni che soddisfi le tue esigenze, leggi le descrizioni di ciascuna delle impostazioni disponibili quando si crea un set di opzioni. Ogni impostazione è spiegata in dettaglio. In alternativa, guarda il nostro video di impostazione del menu qui sopra per vedere come abbiamo creato gli esempi di cui sopra.
{% endhint %}

## Tag piatti

I tag consentono di evidenziare attributi particolari di un piatto con un indicatore visivo completamente personalizzabile. È possibile creare tag per attributi come ad esempio:

* Piccante
* Vegano
* Senza Glutine

Si può creare ogni tipo di tag personalizzato, inclusi gli allergeni. Ogni tag può essere accompagnato da un'icona e da un'abbreviazione.

## Problemi comuni dei menu

### Il menu o le categorie non vengono visualizzati nel ristorane

Affinché il menu venga visualizzato nel tuo ristorante online, assicurati di aggiungere almeno una categoria e un piatto.

### Immagini del piatto troppo grande

Si consiglia vivamente di utilizzare il sito [https://www.birme.net](https://www.birme.net) o [https://tinypng.com/](https://tinypng.com/) per ottimizzare tutte le immagini. Dato che la larghezza massima delle immagini è di 600 pixel circa, è meglio assicurarsi che tutte le immagini non siano più larghe di così. Ciò contribuirà in modo significativo al tempo di caricamento della pagina, soprattutto da smartphone e tablet.
