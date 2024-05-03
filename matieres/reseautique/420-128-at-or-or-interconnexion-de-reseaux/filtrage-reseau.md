---
description: Règles de pare-feu et listes de contrôle d'accès (Sébastien Perron 03/05/2024)
---

# Filtrage réseau

## Que fait le Pare-feu ?

* Le WAN est composé d'inconnus
* Stranger danger
* Prévient la propagation d'un danger
* DST-NAT
* Filtrer le trafic entre les zones
* [#delimiter-des-zones-reseau](filtrage-reseau.md#delimiter-des-zones-reseau "mention")



### Délimiter des zones réseau

{% tabs %}
{% tab title="Réseau étendu" %}
Généralement Internet, réseau sur lequel nous n'avons pas d'autorité
{% endtab %}

{% tab title="Intranet" %}
Réseau local donnant accès aux ressources de l'entreprise
{% endtab %}

{% tab title="Publique" %}
Réseau mis à la disposition des visiteurs donnant généralement accès à Internet et à certains équipements mis à la disposition des visiteurs (imprimantes)
{% endtab %}

{% tab title="Démilitarisée (DMZ)" %}
Zone à sécurité accrue hébergeant les services et serveurs accessibles depuis le réseau étendu)
{% endtab %}
{% endtabs %}

### NGFW: Next-Generation Firewall

* Inspection
* Journalisation
* Protection

## Actions

* Accepter ->  Accepter le trafic et prendre action en conséquence. Soit répondre, NATer, router, etc.
* Bloquer -> Intercepter le trafic et répondre avec un refus de connexion
* Abandonner -> Ignorer le trafic complètement, possible de journaliser (Si face au réseau attendu)

## Conditions

* Source
* Destination
* Protocole
* Port
* Contenu\*

## Pourquoi utiliser un pare-feu?

* Améliorer notre posture en sécurité
* Améliorer la résilience aux pannes de notre réseau
* Optimiser les performances de notre réseau

