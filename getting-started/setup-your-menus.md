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

All **dish customization is done using option sets**. Option sets are a configurable set of options that can be assigned to any number of dishes. With option sets, you are able to create requirements such as:

* Select your pizza crust
* Select one or more sauces
* Select at least 4 toppings

{% hint style="info" %}
To learn how to create an option set that meets your requirements, read the descriptions of each of the settings available when creating an option set. Each setting is explained in detail. Alternatively, watch our menu setup video above to see us create the above examples.
{% endhint %}

## Dish Tags

Tags allow you to highly particular attributes about a dish with a fully customizable visual indicator. You can create tags for attributes such as:

* Spicy
* Vegan
* Gluten free

## Common Menu Problems

### **No menu or categories showing under the store**

For your menu to display in your online store, make sure to add at least one category and one dish to it.

### **Dish images to large**

We highly recommend that you use the website [https://www.birme.net](https://www.birme.net) or [https://tinypng.com/](https://tinypng.com/) to optimize all your images. Given that the maximum image width is only around 600 pixels, it's best to make sure all your images are no wider than that. This is going to help significantly with your page load time especially for mobile customers.
