# Commande MikroTik

## Documentation

Voici la documentation complète sur les appareils MikroTik : [https://wiki.mikrotik.com/wiki/Manual:TOC](https://wiki.mikrotik.com/wiki/Manual:TOC)

## Commandes les plus utilisés

Voici les commandes des appareils MikroTik les plus utilisés:

## Configuration

### Identité

#### Définir le nom

Permet de définir le nom de l'appareil

```
/system/identity/set name=[nom_MikroTik]
```

## Couche 2&#x20;

### Bridge

#### Crée un bridge

Créé un pont auquel il sera possible d'assigner des interfaces

```
/interface/bridge/add name=[nom]
```

#### Assigner un port au bridge

Permet d'assigner un port à un pont

```
/interface/bridge/port/add bridge=[nom_bridge] interface=[nom_port]
```

### VLAN

#### Création d'un VLAN&#x20;

Permet la création d'un VLAN sur une interface, que ce soit un pont ou un port

<pre><code><strong>/interface/vlan/add name=[nom] vlan-id=[numero_vlan] interface=[nom_port ou bridge]
</strong></code></pre>

## Couche 3

### IP

#### Assigner une adresse IP statique

Permet d'assigner une adresse IP à un port, un pont, un VLAN ou tout autre type d'interface

```
/ip/address/add address=[address_IP] interface=[interface]
```

#### Assigner une route statique

Permet la création d'une route statique

```
/ip/route/add dst-address=[réseau de destination]/[masque] gateway=[passerelle à qui envoyer ce trafic]
```

#### Création d'un serveur DHCP

Permet la création accompagnée d'un serveur DHCP

```
/ip/dhcp-server/setup
```
