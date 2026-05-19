# Suivi Dechets - AGRIWATT

PWA mono-fichier pour le suivi du registre dechets reglementaire AGRIWATT
(art. R541-43 du Code de l'environnement).

## Architecture

- `index.html` : application complete (Bootstrap 5, Dexie, jsPDF, SheetJS, MSAL.js)
- `sw.js` : Service Worker (network-first)
- `manifest.json` : manifeste PWA installable

## Donnees

- Stockage local : IndexedDB via Dexie
- Synchronisation : SharePoint (Microsoft Graph API via MSAL.js)
- Dossier SharePoint : `QHSE/Documents/SuiviDechets/`
  - `data.json` : registre principal
  - `presence/` : presence utilisateurs

## Conformite reglementaire

Registre chronologique conforme a l'article R541-43 du Code de l'environnement.
Export Excel avec toutes les colonnes obligatoires : date d'enlevement, code dechet
(LoW), designation, quantite, site producteur, conditionnement, mode de traitement,
numero BSD, transporteur, installation de destination, SIRET destination.

## Deploiement

Voir le repo OVH pour la publication.
