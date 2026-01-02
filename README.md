# Étude de cas : Clients Synchrones (RestTemplate vs Feign vs WebClient) avec Eureka et Consul

Ce projet présente une **étude de cas académique** sur la communication inter-services
dans une architecture **microservices Spring Boot** avec **service discovery**.

Deux microservices sont implémentés :
- **service-client**
- **service-voiture**

La communication est réalisée de manière **synchrone** en utilisant :
- **RestTemplate**
- **Feign Client**
- **WebClient**

Le registre de services est assuré par **Eureka** (et Consul dans une autre configuration).

---

## Démonstration fonctionnelle

Les captures ci-dessous illustrent le bon fonctionnement de l’architecture
et la communication entre les microservices via les différents clients HTTP.


### Eureka – Services enregistrés
Le serveur Eureka affiche les microservices correctement enregistrés et disponibles.

<img width="1918" height="1025" alt="EC-F1" src="https://github.com/user-attachments/assets/080f406c-c0ff-448f-8458-3bc2f3fcbf2e" />


---

### Appel direct du service voiture
Récupération des données voiture associées à un client.

<img width="1919" height="303" alt="EC-F2" src="https://github.com/user-attachments/assets/5555eb2b-df9a-446b-a935-bd5f2c02aaac" />


---

### Appel via RestTemplate
Le service client consomme le service voiture en utilisant **RestTemplate**.

<img width="1919" height="302" alt="EC-F3" src="https://github.com/user-attachments/assets/1670890d-334e-4fae-9cc9-b3b740233d30" />


---

### Appel via Feign Client
Le service client consomme le service voiture via une interface déclarative **Feign**.

<img width="1919" height="290" alt="EC-F4" src="https://github.com/user-attachments/assets/828351b8-2ad0-4f86-8728-885e38cf60a7" />


---

### Appel via WebClient
Le service client consomme le service voiture en utilisant **WebClient**.

<img width="1919" height="278" alt="EC-F5" src="https://github.com/user-attachments/assets/e30b1d6f-8886-4985-83c8-e35d0207656c" />


---

## Objectif pédagogique

Ce projet a pour objectif de :
- Comprendre la **découverte de services** avec Eureka / Consul
- Comparer différentes approches de **clients HTTP synchrones**
- Observer le comportement des microservices en situation réelle
- Préparer une analyse de **performance et de résilience** (détaillée dans le rapport)

Les **analyses détaillées, comparaisons chiffrées et conclusions**
sont disponibles dans le **rapport PDF** associé au projet.
[Étude de Cas.pdf](https://github.com/user-attachments/files/24411582/Etude.de.Cas.pdf)
