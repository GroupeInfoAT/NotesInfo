---
description: Sébastien Perron 03/05/2024
---

# Unités de transmission de données

## Terminologie

**Paquet Ethernet :** Données transmises à la couche physique, contient une trame.

[**Trame Ethernet:**](#user-content-fn-1)[^1] Données transmises à la couche de liaison de données. Mécanisme déterminant le chemin à emprunter dans le domaine de diffusion par adresse MAC de source et destination.

**Paquet IP:** Données transmises à la couche réseau. Mécanisme déterminant le chemin à emprunter à la couche réseau (possiblement sortant du domaine de diffusion).

**MTU**: Maximum Transmission Unit, la taille maximale d'un paquet IP. Généralement 1500 octets.

**Fragmentation IP:** Mécanisme permettant le découpage de paquet IP lorsque la taille d'un paquet excède le MTU.

&#x20;

{% tabs %}
{% tab title="FDB: Forwarding Database" %}
* Table contenue dans un routeur, pont ou commutateur déterminant le prochain saut à utiliser pour éventuellement atteindre l'adresse MAC de destination
* Une par équipement réseau, segmentée par domaines de diffusion
{% endtab %}

{% tab title="ARP: Address Resolution Protocol" %}
* Table contenue dans tous les équipements réseau associant les adresses MAC aux adresses IP
* Une par domaine de diffusion
{% endtab %}
{% endtabs %}

[^1]: Test d'annotage
