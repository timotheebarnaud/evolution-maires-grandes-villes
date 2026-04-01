# LR en recul dans les grandes villes, le PS tient le choc, l'apparition du RN

*Évolution des maires à la tête des 50 plus grandes villes de France entre 2001 et 2026*

## Visualisation

- [Connected dot plot – Flourish](https://public.flourish.studio/visualisation/28224250/)

## Méthodologie

Les données proviennent d'un **scraping de Wikipedia** (`pd.read_html()`) de la page [Liste des maires des grandes villes françaises](https://fr.wikipedia.org/wiki/Liste_des_maires_des_grandes_villes_fran%C3%A7aises), qui recense les maires pour chaque élection municipale de 2001 à 2026. La page ne couvrant que 45 villes, **5 villes ont été complétées manuellement** à partir de sources publiques. Les étiquettes et couleurs politiques ont été **retravaillées manuellement** à partir des données Wikipedia, en s'appuyant sur les conventions de représentation politique habituelles.

Les tooltips affichent le nom du maire et son parti pour chaque année. **Les photos des maires en 2026 sont intégrées pour les 5 premières villes** à titre de prototype ; un déploiement complet nécessiterait de sécuriser les droits d'image, ce qui serait le cas en rédaction.

**Limites** :

La classification politique repose sur un travail éditorial manuel à partir des étiquettes Wikipedia et des classifications du Conseil d'Etat, qui peuvent simplifier des situations locales plus nuancées ou complexes (alliances, dissidences). 

L'analyse se limite aux maires en fonction après chaque élection et ne reflète pas les changements en cours de mandat (hormis le cas de Marseille en 2020 et la passation entre Michèle Rubirola et Benoît Payan, qui figure dans l'infographie).

## Organisation du dépôt

```
├── data/
│   ├── raw/            # Données brutes Wikipedia + compléments manuels
│   └── clean/          # Dataset final (format long : ville × année)
├── notebooks/
│   └── historique_maires_2001_2026.ipynb
└── README.md
```

## Outils

Python (pandas, requests, BeautifulSoup) · Scraping Wikipedia · Jupyter Notebook · Flourish

---

Projet réalisé par **Timothée Barnaud**.
