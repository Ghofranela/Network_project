# 📜 Rapport De Projet 📜

## Parcours  
**ING4-J : SSIR-A**  

## Sujet  
**Architecture et Sécurité de Réseau**  

---

## Réalisé par  
**Meriem Frej & Ghofrane Labidi**  

## 🎓 Encadrant universitaire  
**MR Tarek Hdiji**  

---

## Année Universitaire  
**2024/2025**

---

# Sommaire

- [Introduction Générale](#introduction-generale)
- [Chapitre 1 : Conception et mise en place de VPN-MPLS](#chapitre-1-conception-et-mise-en-place-de-vpn-mpls)
  - [Introduction](#introduction)
  - [Technologie de Service VPN-MPLS](#technologie-de-service-vpn-mpls)
  - [Architecture de la Solution VPN-MPLS](#architecture-de-la-solution-vpn-mpls)
  - [Environnement de travail (GNS3 et VMware)](#environnement-de-travail-gns3-et-vmware)
  - [Topologie de l’entreprise](#topologie-de-lentreprise)
  - [Mise en place de VPN-MPLS de l’entreprise](#mise-en-place-de-vpn-mpls-de-lentreprise)
  - [Validation et test de la connexion](#validation-et-test-de-la-connexion)
- [Conclusion](#conclusion)

---

# Introduction Générale

Dans un monde où la connectivité et la sécurité des réseaux sont devenues des enjeux majeurs pour les entreprises, la conception d’une infrastructure réseau fiable et performante est une nécessité.

Ce projet s'inscrit dans cette problématique en proposant une architecture réseau complète intégrant plusieurs solutions avancées :

- **VPN-MPLS** pour l’interconnexion sécurisée des sites distants tout en optimisant l’acheminement du trafic.
- **Un réseau LAN étendu** pour assurer une haute disponibilité et une gestion efficace des ressources.
- **Une solution de monitoring et de sécurité** permettant d’analyser en temps réel l’état du réseau et de détecter les anomalies.

---

# Chapitre 1 : Conception et mise en place de VPN-MPLS

## Introduction

Le **VPN-MPLS** est une technologie de réseau permettant la création de réseaux privés virtuels à travers une infrastructure de transport MPLS. Contrairement aux VPN traditionnels basés sur **IPSec**, le **VPN-MPLS** s'appuie sur le **routage par labels** pour optimiser l'acheminement du trafic et garantir une meilleure qualité de service.

## Technologie de Service VPN-MPLS

Le VPN-MPLS repose sur plusieurs concepts clés :

- **MPLS (Multiprotocol Label Switching)** : technologie de commutation basée sur des labels permettant d'accélérer le routage des paquets.
- **LDP (Label Distribution Protocol)** : protocole utilisé pour distribuer les labels entre les routeurs MPLS.
- **VRF (Virtual Routing and Forwarding)** : permet d'isoler le routage de différents clients sur un même réseau.
- **MP-BGP (Multiprotocol BGP)** : protocole permettant de propager les informations de routage entre les PE (Provider Edge) dans une infrastructure VPN-MPLS.

## Mise en place de VPN-MPLS de l’entreprise

### Routage OSPF de Backbone IP/MPLS

[![Voir figure](index.md#routage-ospf)](index.md#routage-ospf)

### Configuration de MPLS

[![Voir figure](index.md#configuration-mpls)](index.md#configuration-mpls)

### Configuration de VRF

[![Voir figure](index.md#configuration-vrf)](index.md#configuration-vrf)

## Validation et test de la connexion

### Vérification du routage OSPF

- **Table de voisinage OSPF**  
  [![Voir figure](index.md#table-voisinage-ospf)](index.md#table-voisinage-ospf)

- **Table de routage OSPF**  
  [![Voir figure](index.md#table-routage-ospf)](index.md#table-routage-ospf)

### Vérification des échanges MPLS

- **Affichage des voisins PE1**  
  [![Voir figure](index.md#affichage-voisins-pe1)](index.md#affichage-voisins-pe1)

- **Vérification de la LFIB**  
  [![Voir figure](index.md#verification-lfib)](index.md#verification-lfib)

### Vérification des instances BGP

- **Customer 1 - PE1**  
  [![Voir figure](index.md#customer1-pe1)](index.md#customer1-pe1)

- **Customer 1 - PE2**  
  [![Voir figure](index.md#customer1-pe2)](index.md#customer1-pe2)

### Tests de connectivité entre clients

- **Test de connectivité CE11 à CE12**  
  [![Voir figure](index.md#connectivite-ce11-ce12)](index.md#connectivite-ce11-ce12)

- **Test de connectivité CE21 à CE22**  
  [![Voir figure](index.md#connectivite-ce21-ce22)](index.md#connectivite-ce21-ce22)

---

## Conclusion

Ce chapitre a permis d’introduire la technologie VPN-MPLS et d’expliquer son implémentation dans un environnement simulé. La configuration des routeurs, l’activation de MPLS et la mise en place des VRF sont des étapes essentielles pour assurer une segmentation efficace du trafic. Les tests effectués permettront de valider la robustesse et l'efficacité de cette solution pour l’entreprise.

Le prochain chapitre abordera les résultats obtenus et les conclusions finales sur la performance du VPN-MPLS implémenté.

---

[Retour à l'index](index.md)

