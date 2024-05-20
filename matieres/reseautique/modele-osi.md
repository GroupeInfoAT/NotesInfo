---
description: 17-04-2024 Sébastien Perron
---

# Modèle OSI

Voici la documentation complète en anglais du modèle OSI: [lien](https://en.wikipedia.org/wiki/OSI\_model)

## Définition

**OSI (Open Systems Interconnection)** : Modèle théorique décrivant les composantes et la démarche de communication entre plusieurs appareils informatiques mis en réseau

## Couche du modèle OSI

Voici la liste des couches en ordre:

1. [#physique](modele-osi.md#physique "mention")
2. [#liaison-de-donnees](modele-osi.md#liaison-de-donnees "mention")
3. [#reseau](modele-osi.md#reseau "mention")
4. [#transport](modele-osi.md#transport "mention")
5. [#session](modele-osi.md#session "mention")
6. [#presentation](modele-osi.md#presentation "mention")
7. [#application](modele-osi.md#application "mention")

***

### Physique

* Couche de médium de transport
* Bits
* Équipements réseau
* Interconnexions d'équipements
* Domaines de collision

{% hint style="info" %}
La couche physique: Émet et reçoit les bits individuels composant les trames
{% endhint %}

### Liaison de données

* Couche de médium de transport
* Trames
* Cache de résolution d'adresse (ARP)
* Table de commutation (FIB)
* Domaines de diffusion
* Divisible en sous-couches (LLC et MAC)

{% hint style="info" %}
Couche de liaison de données: Crée les trames et les transporte entre routeurs
{% endhint %}

### Réseau

* Couche de médium de transport
* Cache de résolution d'adresse (ARP)
* Paquets
* Adressage et segmentation IP
* Routage IP

{% hint style="info" %}
Couche de réseau: Créé les paquets, les transporte et les réassemblent
{% endhint %}

### Transport

* Couche d'hôte

Protocoles IP

{% tabs %}
{% tab title="ICMP" %}
ICMP (Internet Control Message Protocol)

* Ping
* Traceroute
{% endtab %}

{% tab title="UDP" %}
UDP (User Diagram Protocol)

* Ne nécessite pas de session
* Sans garantie de livraison
{% endtab %}

{% tab title="TCP" %}
TCP (Transmission Control Protocol)

* Négociation de session
* Fiabilité de livraison
* Vérification d'erreurs
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Couche de transport: Segmente, transmet et réassemble le message du serveur au client
{% endhint %}

### Session

* Couche d'hôte
* Établissement de session
* Contrôle de dialogue
* Synchronisation de communication
* Ex. TCP : SYN, ACK, SYN-ACK, RST, FIN, FIN-ACK

{% hint style="info" %}
Couche de session: Établissement de la connexion entre le serveur et le client
{% endhint %}

### Présentation

* Couche d'hôte
* Syntaxe de données
* Traduction de données
* Liée à la couche d'application

{% hint style="info" %}
Couche de présentation: Le serveur encrypte et compresse le code transmis
{% endhint %}

### Application

* Couche d'hôte
* Spécifique à chaque application
* Contenu de la communication (ex. partage de fichier, transfert de page web, appel vocal, etc.)

{% hint style="info" %}
Couche d'application: Le navigateur demande une page web
{% endhint %}
