# Vidéo

## Matière à couvrir 

* Branchement d’une installation de projection architecturale
* Emploi de protocoles pour transporter la vidéo en temps réel
* Logiciels d'intégration multimédia spécialisés en projection architecturale
* Intégration de médias pour la projection vidéo architecturale
* Optimisation des médias pour la projection vidéo architecturale
* Contrôle de la qualité du produit multimédia
* Archivage du produit multimédia


## Brancher un projecteur

```mermaid
graph TD
    subgraph Source
        PC[Ordinateur PC]
        HDMI[Sortie HDMI]
    end

    subgraph Reseau
        Switch[Switch Ethernet]
    end

    subgraph Extendeur_HDMI
        HDMI_Tx[HDMI Transmetteur]
        CAT6[Cable CAT6]
        HDMI_Rx[HDMI Recepteur]
    end

    subgraph Projecteur
        Proj[Projecteur Video]
        Alim[Alimentation electrique]
        HDMI_IN[Entree HDMI]
        LAN_IN[Port LAN]
        Audio_OUT[Sortie Audio]
    end

    PC -->|Signal HDMI avec audio| HDMI
    Switch --> PC
    HDMI --> HDMI_Tx
    HDMI_Tx -->|CAT6| CAT6
    CAT6 --> HDMI_Rx
    HDMI_Rx --> HDMI_IN


    Switch --> LAN_IN

    Proj -->|Alimentation electrique| Alim

```