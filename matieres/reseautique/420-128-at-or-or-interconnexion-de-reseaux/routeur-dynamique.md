---
description: 12-04-2024 Sébastien Perron
---

# Routeur dynamique

## Définition

Voici la liste des définitions pour les aspects importants du routage dynamique:

<details>

<summary>Liste des définitions</summary>

Voisinage: Lien permettant l'échange de routes entre deux routeurs

Résumer: Regrouper plusieurs réseaux de destination dans une seule route

Sauts: Nombre de routeurs à traverser

Bande passante: Vitesse de lien établi

Fiabilité: Généralement automatique en fonction de stabilité de lien

Charge: Pourcentage d'utilisation du lien

Coût: Valeur administrée à un lien

</details>



## À quoi sert du routage dynamique?

{% tabs %}
{% tab title="Raison de son utilisation" %}
* Faciliter la configuration de routes réseau
* Particulièrement les routes non résumables
* Permettre la redondance automatique de routes
* Optimiser en fonction d'état de liens ou de nombre de sauts l'acheminement de trafic
* Faciliter le déploiement de nouveaux routeurs dans votre réseau
* Faciliter l'extensibilité de votre réseau
{% endtab %}

{% tab title="Danger" %}
* Peut causer des boucles de routage si mal configuré
* Peut être vulnérable à de l'injection de routes malveillantes
* Peut causer de l'instabilité pour l'ensemble du réseau en cas de problème matériel
{% endtab %}
{% endtabs %}



## Types de routage dynamique

* Routage par vecteur de distance
* Routage par état de liens



### Routage par vecteur de distance

* Algorithme basé sur le nombre de sauts
* Reçoit seulement l'information des voisins immédiats périodiquement
* Ne connait pas l'ensemble de la topologie
* Converge très lentement
* Sensible aux boucles de routage
* Simple à mettre en place



#### Protocoles du routage par vecteur de distance

{% tabs %}
{% tab title="Protocole RIP (À éviter)" %}
RIP = Routing Information Protocol

* Protocole de routage par vecteur de distance
* Limité à 16 sauts
* RIPv1 = Diffusion à chaque 30 secondes
* RIPv2 = Multidiffusion
* RIPv2 permet l'authentification
* Désuet
* RIPng ajoute le support pour IPv6
{% endtab %}

{% tab title="Protocole IGRP (À éviter)" %}
IGRP = Internal Gateway Routing Protocol

* Protocole de routage par vecteur de distance
* Propriétaire à Cisco
* «Classful» = Ne supporte pas VLSM, seulement les classes adresses IP
* Diffusion à chaque 90 secondes
* Désuet
* Enhanced IGRP ajoute le support pour VLSM et un algorithme d'évitement de boucles
* Cisco a ouvert EIGRP à d'autres manufacturiers mais est mal implanté par plusieurs
{% endtab %}
{% endtabs %}



### Routage par état de lien

* Algorithme basé sur l'état des liens des routeurs (bande passante, coût, priorité, etc.)
* Tous les routeurs d'une topologie établissent un voisinage
* Mise à jour en multicast seulement lors d'un changement d'état de lien
* Convergence plus rapide
* Plus complexe à mettre en place

#### Protocole du routage par état de lien

{% tabs %}
{% tab title="Protocole IS-IS (NE PAS UTILISER)" %}
IS-IS = Intermediate System to Intermediate System

**NE PAS UTILISER**

* Protocole de routage par état de lien
* Standard très rarement utilisé
* Désuet pas à peu près
{% endtab %}

{% tab title="Protocole OSPF" %}
OSPF = Open Shortest Path Forwarding

* Protocole de routage par état de lien
* Supporté par la majorité des équipements de routage
* Protocole de passerelle interne «IGP» donc l'établissement de routes d'un réseau local
* «Classless» donc supporte tous les masques de sous-réseau
* Voisinage établi par «zones»
* Découverte automatique de voisins
* Supporte l'authentification
{% endtab %}

{% tab title="Protocol BGP" %}
BGP  = Border Gateway Protocol

* Protocole de routage par état de lien
* Supporté sur la majorité des équipements de routage
* Protocole de passerelle externe «EGP» donc l'établissement de routes externes
* Voisinage habituellement distant
* Délimite le réseau local en tant que système autonome
{% endtab %}
{% endtabs %}



#### Système autonome (AS)

* Grand réseau ou groupes réseaux résumables par une politique de routage
* Analogue à un bureau de poste local
* Responsable pour l'acheminement du trafic au sein d'un réseau local où de l'acheminement d'un système autonome à un autre
* Délimite le réseau local du réseau étendu





