# Introduction Générale

Dans un monde où la connectivité et la sécurité des réseaux sont devenues des enjeux majeurs pour les entreprises, la conception d’une infrastructure réseau fiable et performante est une nécessité. Les organisations doivent relever plusieurs défis tels que l’interconnexion sécurisée de sites distants, l’optimisation du trafic, la garantie de la qualité de service et la protection contre les menaces de cybersécurité.

Ce projet s'inscrit dans cette problématique en proposant une architecture réseau complète intégrant plusieurs solutions avancées :

- **VPN-MPLS** pour l’interconnexion sécurisée des sites distants tout en optimisant l’acheminement du trafic.
- **Un réseau LAN étendu** pour assurer une haute disponibilité et une gestion efficace des ressources.
- **Une solution de monitoring et de sécurité** permettant d’analyser en temps réel l’état du réseau et de détecter les anomalies.

L’objectif principal est de concevoir, configurer et tester une infrastructure réseau répondant aux besoins d’une entreprise de grande envergure, tout en garantissant la performance, la scalabilité et la sécurité. Pour cela, nous utiliserons des outils de simulation tels que **GNS3 et VMware**, permettant de reproduire un environnement réseau réaliste.

Ce rapport détaillera chaque phase de mise en œuvre, en commençant par la conception et l’implémentation du VPN-MPLS, puis en explorant la configuration d’un réseau LAN étendu, et enfin en intégrant des solutions de monitoring et de sécurité. L’approche adoptée repose sur une analyse approfondie des technologies utilisées et une validation rigoureuse des performances du réseau.

---

# Chapitre 1 : Conception et mise en place de VPN-MPLS

## Introduction

Le **VPN-MPLS** est une technologie de réseau permettant la création de réseaux privés virtuels à travers une infrastructure de transport MPLS. Contrairement aux VPN traditionnels basés sur **IPSec**, le **VPN-MPLS** s'appuie sur le **routage par labels** pour optimiser l'acheminement du trafic et garantir une meilleure qualité de service.

Ce chapitre présente la technologie **VPN-MPLS**, son architecture, l'environnement de simulation utilisé, ainsi que la topologie réseau mise en place pour notre entreprise fictive.

## Technologie de Service VPN-MPLS

Le VPN-MPLS repose sur plusieurs concepts clés :

- **MPLS (Multiprotocol Label Switching)** : technologie de commutation basée sur des labels permettant d'accélérer le routage des paquets.
- **LDP (Label Distribution Protocol)** : protocole utilisé pour distribuer les labels entre les routeurs MPLS.
- **VRF (Virtual Routing and Forwarding)** : permet d'isoler le routage de différents clients sur un même réseau.
- **MP-BGP (Multiprotocol BGP)** : protocole permettant de propager les informations de routage entre les PE (Provider Edge) dans une infrastructure VPN-MPLS.

## Architecture de la Solution VPN-MPLS

L'architecture d'une solution VPN-MPLS repose sur plusieurs composants essentiels :

- **Routeurs P (Provider Router)** : assurent la commutation des labels et facilitent l’acheminement optimal du trafic MPLS.
- **Routeurs PE (Provider Edge Router)** : connectent les clients et gèrent les **VRF (Virtual Routing and Forwarding)** pour isoler les flux.
- **Routeurs CE (Customer Edge Router)** : connectent les clients aux PE sans gérer directement les labels MPLS.

Ces composants garantissent une connectivité fluide et performante, en minimisant la latence et en optimisant la gestion du trafic.

## Environnement de travail (GNS3 et VMware)

L'implémentation est simulée dans un environnement de test combinant **GNS3** pour la partie réseau et **VMware** pour la virtualisation des hôtes :

- **GNS3** permet de simuler les routeurs et les commutateurs, facilitant l'implémentation de la solution VPN-MPLS.
- **VMware** est utilisé pour créer des machines virtuelles représentant les postes clients et les serveurs de l'entreprise.

## Topologie de l’entreprise

L’entreprise repose sur une architecture MPLS assurant l’interconnexion de plusieurs sites distants via un **backbone IP/MPLS**. La topologie adoptée offre une haute disponibilité, une optimisation du trafic et une séparation des flux clients via des **VRF**.

### Composants clés de la topologie :

- Un **backbone MPLS redondant** reliant les différents sites via des **routeurs de cœur (P routers)**.
- Deux **sites principaux** jouant un rôle central dans la gestion du trafic.
- **Routeurs PE (Provider Edge)** assurant l’attribution des labels et la gestion des VRF.
- **Routeurs CE (Customer Edge)** connectant les clients au réseau MPLS via les PE.
- **MP-BGP** assurant l’échange des routes VPN entre les PE.

[Retour à l'index](index.md)

---

## Mise en place de VPN-MPLS de l’entreprise

### Routage OSPF de Backbone IP/MPLS


### Configuration de MPLS


### Configuration de VRF


## Validation et test de la connexion

### Vérification du routage OSPF

- **Table de voisinage OSPF**  

- **Table de routage OSPF**  

### Vérification des échanges MPLS

- **Affichage des voisins PE1**  

- **Vérification de la LFIB**  

### Vérification des instances BGP

- **Customer 1 - PE1**  

- **Customer 1 - PE2**  

### Tests de connectivité entre clients

- **Test de connectivité CE11 à CE12**  

- **Test de connectivité CE21 à CE22**  

## Conclusion

Ce chapitre a permis d’introduire la technologie VPN-MPLS et d’expliquer son implémentation dans un environnement simulé. La configuration des routeurs, l’activation de MPLS et la mise en place des VRF sont des étapes essentielles pour assurer une segmentation efficace du trafic. Les tests effectués permettront de valider la robustesse et l'efficacité de cette solution pour l’entreprise.

Le prochain chapitre abordera les résultats obtenus et les conclusions finales sur la performance du VPN-MPLS implémenté.

---

[Retour à l'index](index.md)
