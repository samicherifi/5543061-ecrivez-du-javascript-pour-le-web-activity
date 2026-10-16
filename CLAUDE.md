# CLAUDE.md

Ce dépôt est un exercice JavaScript (OpenClassrooms : `index.html`, `blog.html`, `blog.js`, `functions.js`).
Il sert aussi de **base de connaissances pour les projets d'affiliation** (SEO + YouTube, France et international) du propriétaire du dépôt.

## Base de connaissances affiliation — à lire avant tout travail sur le sujet

| Fichier | Contenu |
|---|---|
| `docs/affiliation/01-fondamentaux-business.md` | Modèles de rémunération, plateformes (Amazon, Awin, Impact, PartnerStack…), choix de niche, économie et revente d'un site, légal FR/UE/US, fiscalité |
| `docs/affiliation/02-seo-contenu.md` | Intention d'achat, templates de pages (avis, comparatif, top, alternatives), mises à jour Google 2024-2026, IA, netlinking et ses risques, lancement d'un site neuf, international, stack, GEO |
| `docs/affiliation/03-youtube-video.md` | SEO YouTube, Shorts, chaînes automatisées, politique « contenu inauthentique », divulgation, multilingue, veille avec yt-dlp / vidIQ |
| `docs/affiliation/04-tracking-automatisation.md` | Trackers, EPC/RPM par page, trafic payant, workflows et prompts Claude Code, plan « de zéro au premier revenu » |
| `docs/affiliation/05-analyse-niches-2026-10.md` | Analyse de niches (Ubersuggest + YouTube) du 16/10/2026 et recommandation |

Source d'inspiration initiale : article LinkedIn de Paul Vengeons (12/10/2026) sur l'épisode #146 du podcast MVP avec Franck Marc (Wisewand). Ses chiffres sont **déclaratifs** et les deux auteurs ont des liens commerciaux déclarés (ChatSEO, Wisewand).

Les fiches ont été produites en octobre 2026 par des agents de recherche. Chaque affirmation est étiquetée (fait sourcé / estimation / praticien / incertain). **Revérifier tout chiffre daté avant de s'en servir pour une décision** (taux Amazon, prix des trackers, règles YouTube, dates des mises à jour Google).

## Règles de travail sur les projets d'affiliation

- **Honnêteté sur les chiffres** : ne jamais présenter une estimation comme un fait, ni promettre un revenu. Le propriétaire veut être challengé, pas rassuré.
- **Pas de méthodes à risque sans le dire clairement** : PBN, domaines expirés détournés, contenu produit en masse et chaînes YouTube « inauthentiques » sont contraires aux règles de Google et de YouTube. Les présenter comme des risques, jamais comme une recette.
- **Jamais de fraude** : cookie stuffing, faux clics, faux avis, cloaking trompeur.
- **Conformité** : mention commerciale (loi du 9 juin 2023), case « promotion payée » sur YouTube, divulgation FTC aux US, consentement cookies (CNIL).
- **On mesure en revenu, pas en trafic** : EPC et RPM par page et par vidéo.
- L'IA sert à accélérer (recherche, briefs, code, publication), **pas à remplacer les tests réels** qui font la différence en 2026.

## Outillage dans les sessions cloud

- `pip install yt-dlp` puis `yt-dlp --js-runtimes node ...` : recherche, métadonnées et sous-titres fonctionnent en général. Le téléchargement vidéo est bloqué (403) depuis un datacenter, et YouTube peut parfois exiger une connexion (« not a bot »). En repli : transcriptions via le connecteur vidIQ.
- Connecteurs : vidIQ (YouTube), Ubersuggest (SEO, autorisation OAuth requise dans les réglages claude.ai), Google Drive, GitHub.
