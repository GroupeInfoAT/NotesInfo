# Commande Cisco

## Documentation

Voici la documentation complète sur les appareils Cisco : [https://www.cisco.com/c/en/us/td/docs/switches/lan/catalyst2960x/software/15-2\_2\_e/layer2/command\_reference/b\_Layer2\_3\_1522e\_2960x\_cr.html](https://www.cisco.com/c/en/us/td/docs/switches/lan/catalyst2960x/software/15-2\_2\_e/layer2/command\_reference/b\_Layer2\_3\_1522e\_2960x\_cr.html)

## Commandes les plus utilisés

Voici les commandes des appareils Cisco les plus utilisés:

## Mode Configuration / Globales

Permet d'entrer en mode de configuration (config)# depuis le mode d'exécution

```
configure terminal
```

Permet de sortir du mode de configuration (config)# et retourner au mode d'exécution #&#x20;

<pre><code><strong>end
</strong></code></pre>

Permet d'exécuter une commande à l'intérieur du mode de configuration

<pre><code><strong>(config)# do [commande d'exécution]
</strong></code></pre>

#### !!! WRITE MEMORY !!!

Permet de sauvegarder la configuration pour la préserver suite à un redémarrage. Doit être exécutée en mode d'exécution ou accompagnée de la commande do depuis le mode de configuration

```
write memory
```

Permet de déterminer le nom de l'appareil

```
(config)# hostname
```

Permet de retirer une ligne de configuration

```
no [commande de configuration]
```

## Couche 2

### Interface

#### Entrer dans la configuration d'un interface

Permet d'entrer dans la configuration d'une interface, que ce soit un port ou un VLAN

```
(config)# interface [type_interface] [num_module]/[num_port]
```

#### Crée une interface de routeur

Permet de configurer un port comme une interface de routeur

```
(config-inter)# no switchport
```

#### Désactiver une interface

```
(config-inter)# shutdown
```

### VLAN

#### Crée un VLAN

Permet de déclarer/créer un VLAN

```
(config)# vlan [num_vlan]
```

#### Nommer un VLAN

Permet de nommer un vlan

```
(config-vlan)# name [nom_vlan]
```

#### Faire un TRUNK

Permet de spécifier que le port doit étiqueter les VLANs sur le trafic sortant et tenir compte de celui du trafic entrant.

<pre><code><strong>(config-inter)# switchport trunk encapsulation dot1q
</strong>(config-inter)# switchport mode trunk
(config-inter)# switchport trunk allowed vlan [num_vlans] # Un ou plusieurs numéro de vlan
</code></pre>

#### Faire un ACCESS

Permet de spécifier que le port ne doit pas étiqueter le VLAN sur le trafic sortant et entrant.

```
(config-inter)# switchport mode access
(config-inter)# switchport access vlan [num_vlan]
```

#### Spécifier le VLAN natif

Permet de spécifier un VLAN natif sur un port qui étiquette d'autres VLANs

```
(config-inter)# switchport trunk native vlan [num_vlan]
```

## Couche 3

### IP

#### Assigner une adresse IP statique

Permet de configurer une adresse IP sur une interface, que ce soit un VLAN ou un port de routeur

```
(config-inter)# ip address [adresse_hote] [masque_sous_réseau ex: 255.255.255.0]
```

#### Assigner une route IP statique

Permet de créer une route statique

```
(config)# ip route [adresse_reseau] [masque_sous_réseau] [passerelle]
```

#### Activer les fonctionnalités de couche 3

Permet d'activer les fonctionnalités de niveau 3

```
(config)# ip routing
```
