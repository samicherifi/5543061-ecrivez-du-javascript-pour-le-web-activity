# 02 — SEO & contenu pour l'affiliation (fiche de référence)

> Mémoire durable pour l'assistant. Rédigée le 16 octobre 2026 à partir de recherches web (sources en fin de document).
> Légende utilisée partout : **[Fait]** = sourcé (Google ou presse SEO fiable) · **[Estim.]** = chiffre d'étude ou de vendeur, méthodologie partielle · **[Praticien]** = opinion ou retour d'expérience non démontré · **[Incertain]** = sources contradictoires ou non vérifiées.

---

## Ce qu'il faut retenir

1. **On cible l'intention d'achat, pas le volume.** Trier les requêtes Search Console en « achète / apprend / perdu ». Une courbe de trafic tirée par de l'informationnel ment sur le business. Ordre de priorité : potentiel business > volume > faisabilité.
2. **L'expérience réelle est le seul fossé défensif.** Les sites qui ont survécu aux mises à jour 2023-2026 montrent des tests faits en main propre : photos originales, mesures, défauts assumés, auteur identifiable. Les comparatifs compilés à partir de fiches fabricant se sont effondrés.
3. **Le calendrier Google est chargé et frappe surtout l'affiliation.** Mises à jour core de mars 2025, juin 2025, décembre 2025, mars 2026 et mai 2026. Spam updates d'août 2025, mars 2026, juin 2026 et sept.-oct. 2026. Selon un tracker tiers, 71 % des sites affiliés suivis ont reculé en mars 2026 [Estim.].
4. **L'IA est autorisée, la production de masse sans valeur ajoutée ne l'est pas.** Google juge le résultat, pas l'outil. La politique « scaled content abuse » (mars 2024) s'applique quel que soit le mode de production. Tout passe par une relecture humaine et un fact-check, y compris title, meta, schema et alt.
5. **Pas de programmatique sur un domaine neuf.** On commence par quelques pages solides, puis on publie régulièrement (environ 1 page/semaine au début). On scale seulement quand l'indexation est saine. Les pages « villes » ou « variantes » produites par template ont été ciblées en 2026.
6. **Les liens viennent en dernier, et les PBN restent un pari à haut risque.** Le link spam et l'expired domain abuse sont des violations explicites des règles de Google. Les liens internes sont le levier gratuit : environ 5 liens contextuels vers chaque nouvelle page, depuis des pages de la même thématique.
7. **Il faut construire en anticipant les AI Overviews et l'AI Mode.** Lancés en France le 22 juillet 2026. Le CTR de la position 1 baisse fortement quand un AI Overview s'affiche (−58 % selon Ahrefs [Estim.]). Les requêtes « meilleur X », « A vs B » et « avis » sont exposées. On mesure en conversions, pas en clics.
8. **Le GEO repose d'abord sur le SEO classique.** Google ne demande aucun balisage spécial pour les AI Overviews. Environ 92 % des citations d'AI Overviews viendraient de pages déjà dans le top 10 [Estim.]. Reddit, les avis tiers et les mentions de marque comptent pour ChatGPT et Perplexity.
9. **Pour l'international : un gTLD avec des sous-dossiers par langue, et des hreflang réciproques.** La traduction IA brute, sans recherche de mots-clés locale, produit du contenu mince. Il faut de la transcréation et une relecture native.
10. **Stack : statique et rapide (Astro, ou WordPress headless/optimisé), déployé via GitHub Actions et Cloudflare Pages ou Netlify.** Les liens d'affiliation passent en `rel="sponsored"`. Pour une page « top 10 », on ne compte pas sur les étoiles en rich snippet : une review doit porter sur un seul produit, pas sur une liste.

---

## 1. Intention de recherche et mots-clés transactionnels

### 1.1 Le tri « achète / apprend / perdu » (méthode Franck / Wisewand) [Praticien]
- **Achète** : l'utilisateur est prêt à choisir ou payer. Exemples : « avis X », « X prix », « X vs Y », « alternative à X », « meilleur X 2026 », « code promo X », « X pas cher », « X ou Y », « X arnaque ».
- **Apprend** : intention informationnelle (« comment… », « qu'est-ce que… »). Ces pages servent au maillage et à l'autorité thématique, rarement à la conversion directe.
- **Perdu** : requêtes hors sujet, de navigation vers une autre marque ou sans valeur. On les ignore, voire on désoptimise la page.
- Si la majorité des clics est en « apprend » ou « perdu », la courbe GSC est trompeuse.

### 1.2 Familles de requêtes « argent » (par ordre typique de conversion)
| Requête | Intention | Format de page |
|---|---|---|
| `code promo X`, `X réduction` | Achat imminent | Page coupon (attention : les agrégateurs programmatiques de coupons ont été très touchés en 2026 [Estim.]) |
| `X avis`, `X test`, `X arnaque` | Validation avant achat | Review d'un seul produit |
| `X vs Y`, `X ou Y` | Choix final | Comparatif face-à-face |
| `alternative à X`, `X concurrent` | Insatisfaction et recherche active | Page « alternatives » |
| `X prix`, `X tarif` | Évaluation du budget | Section prix (ou page dédiée), tableau de plans |
| `meilleur X 2026`, `top X` | Shortlist | Best-of / top |
| `quel X choisir`, `guide achat X` | Exploration | Guide d'achat (hub vers les pages ci-dessus) |

### 1.3 Méthode Search Console (actionnable)
1. Performance > Requêtes > filtre **Regex personnalisée** (moteur RE2 : pas de lookahead ni de backreference [Fait]). Exemple pour le français :
   `\b(avis|test|prix|tarif|meilleur|meilleure|top|vs|alternative|comparatif|code promo|promo|réduction|pas cher|acheter)\b`
   Pour l'anglais : `\b(best|review|vs|alternative|price|pricing|coupon|discount|cheap|buy)\b`
2. Utiliser la même regex en mode « Ne correspond pas » pour isoler l'informationnel et le perdu. Exporter, puis comparer clics achat / clics totaux.
3. **Quick wins** : requêtes « achète » en position 5 à 20 avec des impressions réelles (seuil pratique : ≥100 impressions sur 3 mois [Praticien]). Actions : enrichir la page, ajuster title et H1, ajouter des liens internes. Toucher d'abord aux pages âgées de plus de 90 jours.
4. Avant d'écrire, regarder la SERP des 10 mots-clés cibles. Si elle est occupée par Shopping, des vidéos, des forums ou un AI Overview massif, choisir un autre format (une vidéo YouTube, par exemple) ou une autre requête [Praticien, article Franck].
5. Priorité finale : **potentiel business** (commission × taux de conversion estimé) > volume > faisabilité (DR et nombre de domaines référents des pages du top 3).

---

## 2. Types de pages qui convertissent : templates

Les recommandations officielles de Google pour les reviews [Fait] servent de cahier des charges : évaluer du point de vue de l'utilisateur, montrer son expertise, apporter des **preuves d'expérience directe** (photos, vidéo, audio, liens), donner des **mesures quantitatives**, expliquer ce qui différencie le produit, couvrir les alternatives, avantages et inconvénients issus de recherche originale, l'évolution par rapport aux modèles précédents, **proposer plusieurs marchands**, justifier les « meilleur pour… » par des preuves, et rendre les listes classées utiles même sans les reviews détaillées. La qualité et l'originalité priment sur la longueur.

### 2.1 Review d'un produit (« X avis »)
```
H1 : X avis (2026) : notre test après N semaines
[Encadré verdict au-dessus de la ligne de flottaison]
  - Note /10 + phrase verdict + « Pour qui / Pas pour qui »
  - CTA principal (bouton) + prix constaté + date de vérification
[Preuve de test] photo originale / capture de l'outil avec nos données
H2 : Notre méthode de test (durée, conditions, critères, ce qu'on a mesuré)
H2 : Points forts / Points faibles (vrais défauts, pas « un peu cher »)
H2 : Résultats mesurés (tableau de chiffres)
H2 : Prix et formules (tableau, date de mise à jour) → CTA
H2 : X vs alternatives (mini-tableau + liens internes vers les comparatifs)
H2 : Pour qui ? (profils)
H2 : FAQ (vraies questions issues de GSC, PAA, forums)
Encadré auteur (nom réel, bio, pourquoi il est légitime) + divulgation d'affiliation
```

### 2.2 Comparatif face-à-face (« X vs Y »)
- Verdict immédiat : « Choisissez X si…, Y si… » avec **2 CTA**.
- Tableau comparatif de 8 à 12 critères. Une colonne « gagnant » par ligne.
- Tests côte à côte (mêmes conditions, mêmes mesures) et captures.
- Prix réels, coûts cachés.
- Liens internes vers la review de X, celle de Y, et la page best-of.

### 2.3 Best-of / top (« meilleur X 2026 »)
```
H1 : Les N meilleurs X en 2026 (testés)
Intro courte : critères + combien de produits testés + date de mise à jour
Tableau récapitulatif : rang | produit | « meilleur pour » | note | prix | CTA
Pour chaque produit (H2 : n°1 — Produit : meilleur pour <usage>) :
  - Photo originale, 3 pour / 2 contre, verdict, CTA, lien vers la review complète
H2 : Comment nous avons testé (méthodologie publique, réutilisée sur le site)
H2 : Guide d'achat (critères qui comptent vraiment)
H2 : Produits écartés et pourquoi (signal fort d'expérience réelle)
FAQ + auteur + divulgation
```

### 2.4 Page « alternatives à X »
- Pourquoi les gens quittent X (douleurs réelles, citations d'avis, forums).
- 5 à 10 alternatives classées par cas d'usage, chacune avec un CTA.
- Tableau de migration (fonctionnalités, prix, facilité de migration).

### 2.5 Guide d'achat (« quel X choisir »)
- Page hub informationnelle orientée vers l'achat. Elle explique les critères, puis renvoie vers le best-of, les reviews et les comparatifs.

### 2.6 Placement des CTA et des liens (bonnes pratiques)
- **Premier CTA visible sans scroll**, dans l'encadré verdict. Ensuite un CTA après chaque bloc produit, un dans le tableau et un en conclusion [Praticien, consensus].
- Les boutons convertissent mieux que les liens texte [Praticien]. On garde aussi des liens texte contextuels.
- Les liens affiliés portent `rel="sponsored"` (ou `nofollow`) [Fait, Google]. On les fait passer par un `/go/slug` redirigé, ou par un tracker si plusieurs pays sont visés (voir la fiche monétisation).
- **Plusieurs marchands** quand c'est possible : recommandation explicite de Google [Fait].
- Divulgation d'affiliation visible en haut de page. C'est une obligation légale en France pour la publicité (loi influenceurs de 2023, DGCCRF). À vérifier dans la fiche juridique.
- Tableaux : HTML natif (pas d'images), lisibles sur mobile (défilement horizontal du tableau seul, ou cartes empilées). Afficher la date de vérification des prix.

### 2.7 Preuves de test réel (checklist E-E-A-T)
- [ ] Photos et vidéos **originales** (pas de visuels fabricant), avec EXIF ou contexte crédible
- [ ] Captures d'écran avec nos propres données (logiciels, SaaS)
- [ ] Mesures chiffrées (autonomie, vitesse, bruit en dB, temps de réponse du support…)
- [ ] Durée et conditions de test précisées
- [ ] Défauts réels + « produits écartés »
- [ ] Auteur nommé, page auteur, compétence vérifiable (LinkedIn, autres publications)
- [ ] Page « Méthodologie de test » unique, liée depuis chaque review
- [ ] Date de mise à jour réelle (pas un simple changement de date)
- [ ] Mentions légales, page « À propos », contact, politique d'affiliation

---

## 3. Google 2023-2026 : chronologie et leçons

### 3.1 Chronologie [Fait sauf mention contraire]
| Date | Événement | Effet sur l'affiliation |
|---|---|---|
| Fév.-mars 2023 | Product Reviews Update (21 fév. → mars) | Dernière mise à jour « product reviews » |
| 12-25 avr. 2023 | Reviews Update : le système couvre tous les types d'avis (services, entreprises, médias…) | Ensuite, les mises à jour reviews se fondent dans les core updates [Incertain sur la date exacte de fusion] |
| 14-28 sept. 2023 | **Helpful Content Update** | Nombreux sites de niche affiliés effondrés. Exemple : HouseFresh, environ −95 % du trafic Google (4 000 → environ 200 visites/jour) |
| 5 mars 2024 | Core update + intégration du système Helpful Content au core. Nouvelles politiques : **scaled content abuse, expired domain abuse, site reputation abuse** | Fin des « HCU » séparées. La récupération passe par les core updates |
| 7 mai 2024 | Début des actions manuelles pour site reputation abuse (parasite SEO) | Coupons et sections « best » hébergés sur des médias pénalisés |
| Nov. 2024 | Site reputation abuse : suppression de l'exception « supervision first-party » | Le contenu tiers est en violation même s'il est supervisé |
| Août 2024 | Core update : premières récupérations partielles (HouseFresh) | — |
| 13-27 mars 2025 | Core update | — |
| 30 juin-17 juil. 2025 | Core update | — |
| 26 août-22 sept. 2025 | Spam update (large) | — |
| 11-29 déc. 2025 | Core update | Tracker tiers : environ 71 % des affiliés touchés [Estim.] |
| Mars 2026 (environ 24-25) | Spam update très rapide (moins de 20 h) | Pages programmatiques et templates « villes » touchées [Estim.] |
| 27 mars-8 avr. 2026 | Core update | **71 % des sites affiliés suivis en baisse** (JetDigitalPro, plus de 600k pages), −20 à −35 % typiquement [Estim., source unique] |
| 21 mai-2 juin 2026 | Core update | — |
| 24-26 juin 2026 | Spam update | Visait des sites qui n'apportent que des descriptions produits et des liens affiliés [Estim.] |
| 22 juil. 2026 | **AI Overviews et AI Mode lancés en France** | Voir §8 |
| 24 juil. 2026 | Règle review snippets : avis incités non divulgués interdits (action manuelle possible) [Estim. sur la date ; la règle figure bien dans la doc] | — |
| 30 août 2026 | Site reputation abuse : les actions manuelles **n'affectent plus les résultats dans l'EEE** (après l'enquête DMA de la Commission, ouverte le 13 nov. 2025). La politique s'applique toujours hors EEE | Le parasite SEO redevient tentant en Europe, mais le risque reste algorithmique et hors UE. À suivre |
| Sept.-8 oct. 2026 | Spam update (environ 13 jours) | « Normal spam update » selon Google. Cas de sites Amazon minces programmatiques touchés (GSQi) |

Une « July 2026 core update » apparaît sur certains blogs mais **n'est pas confirmée** [Incertain]. Il faut vérifier sur le Google Search Status Dashboard.

### 3.2 Ce qui a tué les sites affiliés [synthèse Fait + Estim.]
- **Thin affiliation** (règle explicite de Google) : des fiches produit réécrites avec des liens affiliés, sans valeur ajoutée.
- Reviews et top « de bureau » : compilation de specs et d'avis Amazon, aucune preuve de test.
- Volume IA non relu, templates massifs (comparatifs automatiques, pages villes, agrégateurs de coupons).
- Parasite SEO sur des domaines tiers (une stratégie qui s'est éteinte d'un coup en mai 2024).
- Profils de liens manipulés (PBN, guest posts payés en dofollow), neutralisés par les spam updates.
- Sites « sans visage » : pas d'auteur, pas d'entité réelle, pas de signaux de marque.

### 3.3 Ce qui survit [Estim. / Praticien convergents]
- Tests réels documentés, photos et vidéos originales, défauts assumés, auteur vérifiable.
- Sites de niche **étroite** avec une vraie expertise, et une marque qui génère des recherches navigationnelles.
- Diversification des canaux : YouTube, newsletter, réseaux sociaux. Le trafic Google n'est plus la seule base.
- Mise à jour réelle des contenus (prix, nouveaux modèles), plutôt que des changements cosmétiques de date.

### 3.4 Récupération
- Il n'y a plus d'« HCU » à attendre. Une amélioration ne se voit qu'aux core updates suivantes (plusieurs mois) [Fait, Google]. HouseFresh a mis environ 2 ans à récupérer en partie [Fait].
- Plan : auditer page par page (trafic, conversions, qualité) → supprimer, fusionner ou noindex les pages faibles → réécrire les pages à fort potentiel avec de vraies preuves → renforcer auteur et marque.

---

## 4. Contenu IA : position de Google et bonnes pratiques

### 4.1 Position officielle [Fait]
- L'IA générative est acceptable pour la recherche et la structuration de contenu original. **Générer de nombreuses pages sans valeur ajoutée** peut violer la politique scaled content abuse. Celle-ci s'applique quelle que soit la méthode de production (IA, rédacteurs humains, template).
- Fact-checker tout, y compris les **title, meta descriptions, données structurées et alt d'images**.
- Envisager d'indiquer comment le contenu a été produit.
- E-commerce : les images générées par IA doivent porter la métadonnée IPTC `DigitalSourceType = TrainedAlgorithmicMedia` (Merchant Center).
- Les Quality Rater Guidelines (sections 4.6.5 et 4.6.6) décrivent le scaled content abuse et le contenu peu original.
- Aucun seuil (pages/jour, ratio) n'est publié [Fait].

### 4.2 Règles d'usage pour l'assistant (process recommandé) [Praticien]
1. **L'humain fournit la matière** : notes de test, photos, mesures, avis. L'IA structure, rédige, traduit et vérifie la cohérence. Sans matière humaine, pas de page « argent ».
2. Brief par page : intention, requête cible, SERP analysée, angle différenciant, données propriétaires à inclure.
3. Relecture humaine obligatoire : faits, prix, specs, ton, suppression des formules creuses typiques de l'IA (« dans un monde en constante évolution… »).
4. Une page par exécution dans la file de publication, avec contrôle de doublons et de cannibalisation (règle de Franck) [Praticien].
5. Ne pas publier de pages qui reformulent les 10 premiers résultats sans rien ajouter. C'est exactement l'exemple de scaled content abuse.
6. Garder un journal des sources pour chaque affirmation chiffrée.

---

## 5. Netlinking : honnêteté sur les risques

### 5.1 Ce que dit Google [Fait]
- **Link spam** : créer des liens vers ou depuis un site principalement pour manipuler le classement. Les exemples cités incluent l'achat ou la vente de liens, les articles sponsorisés et guest posts avec ancres optimisées, et les liens de footer ou de widget.
- **Expired domain abuse** : acheter un domaine expiré et le réutiliser principalement pour manipuler le classement avec du contenu de faible valeur.
- Les liens issus de guest posts, de contenu sponsorisé ou d'affiliation doivent porter `rel="sponsored"` ou `nofollow`. Actions manuelles possibles en cas d'abus.
- Les PBN ne sont pas nommés tels quels, mais relèvent clairement du link spam (liens créés pour manipuler).

### 5.2 PBN (réseaux de sites privés)
- **Pratique de Franck** [Praticien] : domaines expirés non vendus aux enchères (environ 10 €) avec un peu d'historique. Un article par jour par site via Wisewand, Claude et MCP. Les sites du réseau génèrent aussi du trafic (100 à 1 000+ clics/jour) et convertissent. Dimensionnement : rester dans la fourchette du nombre de liens des 3 premiers résultats.
- **Réalité du risque** : violation explicite. Les spam updates (SpamBrain) neutralisent ou pénalisent les réseaux, et un footprint commun (hébergement, template, WHOIS, maillage croisé, Search Console partagée) peut faire tomber l'ensemble. Les gains sont réels pour certains praticiens, mais **non démontrés publiquement** et réversibles du jour au lendemain.
- **Position de l'assistant** : ne pas recommander de PBN sur un « money site » qu'on veut revendre ou garder longtemps. Si l'utilisateur choisit de le faire, l'informer du risque, ne jamais mettre en danger le site principal, et isoler les expérimentations.

### 5.3 Domaines expirés : où les trouver et comment les évaluer
- **Sources** : expireddomains.net, enchères des registrars (GoDaddy Auctions, NameJet, Dynadot, Sedo), backorders, et l'AFNIC pour les `.fr` (domaines tombés dans le domaine public).
- **Checklist d'évaluation** (en partie issue de l'article Franck/Paul et de guides de registrars) :
  - [ ] Wayback Machine : historique propre et **cohérent thématiquement**, surtout les 2-3 dernières années. Rejeter les domaines passés par casino, pharma, adulte, ou du contenu chinois ou japonais
  - [ ] `site:domaine.tld` : résultats indexés hors sujet ou en langue étrangère = mauvais signe
  - [ ] Backlinks (Ahrefs, Majestic, Semrush) : liens éditoriaux réels, thématiques proches, ancres naturelles. Rejeter si dominé par annuaires, commentaires de spam ou ancres sur-optimisées
  - [ ] Google Safe Browsing / listes noires
  - [ ] Marque déposée (risque UDRP / INPI)
  - [ ] **Ne pas se fier au DR, DA, TF ou trafic estimé**, qui sont manipulables [Praticien]. Les domaines les plus « abusables » ont souvent de bons scores
- **Usage légitime** : reprendre le domaine pour le **même sujet**, avec un contenu de qualité supérieure, ou rediriger en 301 vers une page équivalente pertinente. L'usage abusif (domaine d'une association repris en casino) est précisément la cible de la politique.

### 5.4 Guest posts et relations presse
- Un guest post sur un site éditorial réel, pour la visibilité et la marque : OK. Selon Google, ses liens devraient porter sponsored ou nofollow.
- Alternatives plus sûres : digital PR (études et données originales, baromètres), citations d'expert, partenariats, contenus « linkables » (outils, calculateurs, données de test). Les mentions de marque comptent aussi pour le GEO (§8).

### 5.5 Maillage interne (levier gratuit n°1)
- **Règle de Paul (article)** [Praticien] : 5 liens internes vers chaque nouvelle page, depuis des pages de la même thématique, avec la requête comme ancre (en variant les formulations pour rester naturel).
- Architecture en silos : guide d'achat (hub) → best-of → reviews et comparatifs, avec des liens croisés entre reviews et comparatifs du même produit.
- Pas de page orpheline. Fil d'Ariane avec le schema `BreadcrumbList`.
- Lors de chaque publication, l'assistant ajoute automatiquement les liens entrants dans des pages existantes et pertinentes (pas seulement les liens sortants).

---

## 6. Lancer un site neuf

### 6.1 Délais réalistes
- Ahrefs (étude ancienne) : seulement 5,7 % des pages atteignaient le top 10 en un an, la plupart en 61 à 182 jours. Une mise à jour 2025 relayée par des blogs parle de 1,74 % [Incertain]. Âge moyen d'une page top 10 : 2 ans et plus [Fait/Estim.].
- « Sandbox » : jamais confirmée officiellement. Des propos attribués à Google évoquent qu'il faut parfois jusqu'à un an pour situer un nouveau site [Incertain]. En pratique, compter **6 à 12 mois** avant un trafic significatif sur une niche concurrentielle [Praticien].
- Ne pas juger ni modifier une page avant **environ 90 jours** [Praticien, Paul].

### 6.2 Rythme de publication [Praticien, article]
- Site neuf : **environ 1 page/semaine** de grande qualité (Paul). Site établi : 2 à 4/semaine. Réseau ou site refait : 1/jour (Franck).
- Principe : **copier la régularité, pas le volume**. Le rythme doit correspondre à la confiance que Google accorde déjà au domaine.

### 6.3 Séquence de lancement (checklist)
1. Choisir l'offre et vérifier commissions, pays et cookie (voir la fiche monétisation).
2. Lister 20 à 50 requêtes « achète », analyser leurs SERP (formats présents, AI Overview, forums).
3. Pages de confiance : À propos, Méthodologie de test, Auteur(s), Contact, Mentions légales, Politique d'affiliation.
4. Publier 5 à 10 pages argent **faites à la main et parfaites** (template de référence), puis seulement après écrire le process et le template pour dupliquer.
5. Ajouter des pages informationnelles de soutien pour le maillage.
6. GSC et sitemap dès le premier jour. Suivre **taux d'indexation** et motifs « Détectée/Explorée, actuellement non indexée ».
7. À 3 mois : quick wins sur les positions 5-20, maillage et enrichissements.
8. Scaler (plus de rythme, puis programmatique) **seulement si** l'indexation dépasse environ 80 % des pages soumises et que les pages argent progressent [seuil Praticien].

### 6.4 SEO programmatique bien fait
- Franck : le programmatique sur un domaine neuf est un « soufflé » qui monte puis retombe [Praticien]. Exemple d'indexation : une construction de 287 000 pages sur un domaine neuf a obtenu environ 0,9 % de pages indexées [Estim., anecdote].
- Conditions pour que ça marche :
  - [ ] **Données propriétaires ou réellement agrégées** différentes pour chaque page (prix relevés, tests, specs normalisées, avis collectés). Changer seulement le nom de ville ou de produit ne suffit pas
  - [ ] Chaque page répond à une requête réelle avec de la demande (vérifiée dans les outils et GSC)
  - [ ] Démarrer par 20 à 30 pages, vérifier l'indexation, puis augmenter par lots
  - [ ] Pas de pages vides ou quasi-vides (noindex tant que la donnée est insuffisante)
  - [ ] Liens internes logiques (facettes, hubs), pas des milliers de pages orphelines
- Les exemples connus (Zapier, environ 70 000 pages d'intégration) reposent sur une marque et une autorité énormes, pas sur la technique seule [Estim.].

---

## 7. SEO international et multilingue

### 7.1 Structure d'URL (tableau Google) [Fait]
| Option | Avantages | Inconvénients |
|---|---|---|
| ccTLD (`exemple.de`) | Ciblage géographique clair, sites séparés | Coût, infra, un seul pays, l'autorité repart de zéro |
| Sous-domaine (`de.exemple.com`) | Facile, serveurs séparés possibles | Ambiguïté langue/pays |
| **Sous-dossier (`exemple.com/de/`)** | Facile, un seul hôte, l'autorité est partagée | Signal géographique plus faible, séparation plus difficile |
| Paramètre (`?loc=de`) | — | **Non recommandé** |

**Recommandation pour l'affiliation** : un gTLD neutre (`.com`) avec un sous-dossier **par langue** (`/fr/`, `/en/`, `/es/`). C'est aussi le conseil de Franck. On passe au ccTLD seulement si une marque locale forte ou une contrainte juridique le justifie.

### 7.2 hreflang : checklist
- [ ] Chaque version liste **toutes** les versions, **y compris elle-même** (réciprocité). Sans réciprocité, Google ignore les balises
- [ ] Codes ISO valides (`fr`, `fr-BE`, `en-GB`, `es-MX`) + `x-default`
- [ ] Canonical vers soi-même dans chaque langue (jamais vers la version d'une autre langue)
- [ ] Implémentation dans le `<head>` ou dans le sitemap (le sitemap est plus fiable à grande échelle)
- [ ] Pas de redirection automatique par IP (laisser un sélecteur de langue)

### 7.3 Traduction IA
- Google n'a rien publié de spécifique sur la traduction automatique dans ces documents. Il faut appliquer la logique du scaled content : une traduction brute sans valeur ajoutée est risquée [Estim., consensus praticiens].
- Process : **recherche de mots-clés locale** (les requêtes diffèrent : « avis » / « review » / « opiniones »), offres et marchands locaux, prix en devise locale, relecture par une personne native, adaptation des exemples (transcréation).
- Ne traduire que les pages qui ont une demande et une offre affiliée dans le pays cible. Vérifier aussi la SERP locale (moins de concurrence possible : argument de Franck sur les marchés non anglophones).

---

## 8. AI Overviews, AI Mode et GEO/AEO

### 8.1 Impact sur le trafic
- **France : lancement le 22 juillet 2026** (desktop, mobile, app). C'était le dernier grand marché d'Europe de l'Ouest, avec un retard lié aux droits voisins [Fait].
- Ahrefs (300k mots-clés, déc. 2023 vs déc. 2025) : **CTR de la position 1 en moyenne −58 %** quand un AI Overview est présent [Estim.]. Pew : 8 % de clics avec un résumé IA, contre 15 % sans [Estim.].
- Expérience randomisée (UPenn/Northeastern, arXiv, août 2026) : l'AI Mode réduit les clics sortants d'environ 18,8 points [Estim., étude sérieuse avec limites].
- Selon Google, les clics venant de pages avec AI Overviews sont « de meilleure qualité », et ce trafic est compté dans GSC (type de recherche « Web »), sans segment dédié [Fait].
- Conséquence : on suit **les conversions et revenus par page**, pas seulement les clics. On cible davantage les requêtes à forte spécificité (modèle précis, cas d'usage, local, code promo) et la marque.

### 8.2 Être cité : ce que dit Google [Fait]
- **Aucune exigence technique supplémentaire**, aucun fichier IA ni schema spécial. Une page indexée et éligible au snippet peut être citée.
- Le « query fan-out » lance des sous-requêtes. Couvrir les sous-questions (prix, alternatives, pour qui, défauts) augmente les chances d'être cité.
- Bonnes pratiques : autoriser le crawl (y compris via le CDN, attention aux règles anti-bots de Cloudflare), maillage interne, contenu important en texte, images et vidéos de qualité, structured data cohérente avec le texte visible.
- Contrôles : `nosnippet`, `data-nosnippet`, `max-snippet`, `noindex`. `Google-Extended` concerne l'entraînement et le grounding des autres produits Google, pas Search.
- Les politiques anti-spam couvrent aussi la manipulation des réponses génératives de Google [Fait].

### 8.3 GEO pour ChatGPT et Perplexity [Estim., données de vendeurs à prendre avec prudence]
- Les sources citées varient fortement selon le moteur : environ 11 % seulement de domaines communs entre ChatGPT et Perplexity. Reddit domine Perplexity et les AI Overviews. Wikipedia et Reddit pèsent pour ChatGPT.
- Environ 92 % des citations d'AI Overviews viennent de pages du top 10 organique. **Le SEO classique reste la base.**
- Leviers actionnables :
  - Paragraphe-réponse en tête de section (40-60 mots, phrase autonome citable), verdicts explicites (« meilleur pour X : Y, parce que… »).
  - Tableaux et données chiffrées originales (les LLM citent volontiers des chiffres uniques).
  - Fraîcheur visible (date de mise à jour, « 2026 » dans le title quand c'est pertinent). L'effet est revendiqué par des vendeurs, il n'est pas prouvé.
  - Mentions de marque hors site : Reddit et forums (participation authentique, pas de spam), YouTube, presse, comparateurs.
  - Autoriser `OAI-SearchBot`, `PerplexityBot` et `ChatGPT-User` dans robots.txt si l'on veut être cité (à distinguer des bots d'entraînement comme `GPTBot`).
- Mesure : trafic referral `chatgpt.com` et `perplexity.ai` dans GA4, et suivi de prompts via un outil GEO.

---

## 9. Stack technique

### 9.1 CMS
| Option | Pour | Contre |
|---|---|---|
| WordPress classique | Écosystème, plugins affiliation et SEO, rédaction facile | Performance variable, maintenance et sécurité, dette de plugins |
| WordPress headless + front Astro/Next | Édition WP + front rapide | Complexité double |
| **Astro (contenu Markdown/MDX dans Git)** | Très rapide, HTML statique, idéal pour Claude Code + GitHub (une page = un fichier, PR, CI) | Pas d'interface d'édition pour des non-devs (on peut ajouter un CMS Git : Decap, Tina, Keystatic) |

- Core Web Vitals : selon les données HTTP Archive et CrUX relayées, Astro passe environ 15 à 25 points plus souvent que WordPress (ex. 60 % contre 38 % sur mobile) [Estim., chiffres variables]. Les CWV sont un signal mineur de classement, mais elles comptent pour la conversion. Seuils « bons » : **LCP ≤ 2,5 s, INP ≤ 200 ms (remplace FID depuis le 12 mars 2024), CLS ≤ 0,1**.
- Choix par défaut pour l'assistant : **Astro + contenu en Git**, comme dans la refonte de Franck [Praticien]. Garder WordPress si l'utilisateur a déjà un site qui rapporte.

### 9.2 Déploiement
- Repo GitHub → **Cloudflare Pages** ou **Netlify** (déploiement à chaque push, préviews de PR).
- Publication planifiée : **GitHub Actions** en cron qui prend la prochaine page d'une file (`content/queue/`), vérifie les doublons, applique le template, injecte les liens internes et le schema, met à jour le sitemap, déploie, puis valide l'URL en ligne (HTTP 200, indexabilité) [Praticien, article].
- **Migration ou refonte** : exporter d'abord toutes les URL avec des clics (GSC 16 mois), conserver URL, title et H1, ou faire des 301 page à page. Vérifier ensuite la couverture dans GSC.

### 9.3 Schema.org pour l'affiliation
- Utiles : `Article`/`BlogPosting` (auteur, dates), `Person` (page auteur), `Organization`, `BreadcrumbList`, `FAQPage` (n'affiche presque plus de rich result pour la plupart des sites, mais aide à la structure), `ItemList` pour les tops.
- **Review / Product** [Fait, doc Google] :
  - Une review doit porter sur **un élément précis**, **pas sur une catégorie ou une liste** : pas d'étoiles sur la page « top 10 » elle-même.
  - `author` obligatoire (vrai nom, moins de 100 caractères).
  - **Interdit** : agréger des avis ou notes d'autres sites (copier les étoiles Amazon ou Trustpilot dans le schema). Interdit aussi : les avis faux ou incités non divulgués.
  - La règle « self-serving » concerne `LocalBusiness` et `Organization` (une entité qui note elle-même). Une review éditoriale d'un produit tiers sur un site affilié reste éligible en principe, mais **l'affichage n'est jamais garanti**.
  - Le contenu balisé doit être visible sur la page. On ne balise que la note que l'on attribue soi-même.
- Valider avec le Rich Results Test. Le schema doit correspondre exactement au texte (Google le rappelle aussi pour les fonctionnalités IA).

---

## 10. Checklist « page argent » avant publication (résumé opérationnel)
- [ ] Requête « achète » validée (GSC ou outil), SERP analysée, format adapté
- [ ] Pas de cannibalisation avec une page existante
- [ ] Verdict et CTA au-dessus de la ligne de flottaison, divulgation d'affiliation visible
- [ ] Preuves de test originales (au moins 3 photos ou captures maison, mesures chiffrées)
- [ ] Tableau comparatif HTML responsive, prix datés, plusieurs marchands si possible
- [ ] Section défauts, « pour qui / pas pour qui », alternatives
- [ ] Auteur nommé et lien vers la méthodologie
- [ ] Liens affiliés en `rel="sponsored"`, passant par `/go/` ou un tracker
- [ ] Au moins 5 liens internes entrants ajoutés depuis des pages de la même thématique + liens sortants vers hub et reviews
- [ ] Title (moins de 60 caractères, avec l'année si c'est une requête fraîche), meta, H1 et alt relus par un humain
- [ ] Schema valide et cohérent (pas d'étoiles sur une liste)
- [ ] LCP < 2,5 s sur mobile, images en AVIF/WebP dimensionnées
- [ ] Sitemap mis à jour, URL vérifiée en ligne, inspection GSC si besoin
- [ ] Ne plus toucher pendant 90 jours, sauf erreur factuelle ou changement de prix

---

## Sources

**Article de départ**
- Paul Vengeons, « Affiliation SEO : la machine à 20k€/mois de Franck, avec Claude Code » (LinkedIn, 12 oct. 2026). Témoignage non vérifié, sponsorisé par ChatSEO : https://fr.linkedin.com/pulse/affiliation-seo-la-machine-%C3%A0-20kmois-de-franck-avec-claude-vengeons-rq2we

**Google (sources primaires)**
- Spam policies : https://developers.google.com/search/docs/essentials/spam-policies
- Write high quality reviews : https://developers.google.com/search/docs/specialty/ecommerce/write-high-quality-reviews
- Using generative AI content : https://developers.google.com/search/docs/fundamentals/using-gen-ai-content
- AI features and your website : https://developers.google.com/search/docs/appearance/ai-features
- Review snippet structured data : https://developers.google.com/search/docs/appearance/structured-data/review-snippet
- Managing multi-regional sites : https://developers.google.com/search/docs/specialty/international/managing-multi-regional-sites
- Regex dans Search Console : https://developers.google.com/search/blog/2021/06/regex-negative-match

**Mises à jour et politiques**
- SEJ, mise à jour core de mars 2026 terminée : https://www.searchenginejournal.com/google-confirms-march-2026-core-update-is-complete/571459/
- SEL, mise à jour core de mai 2026 terminée : https://searchengineland.com/google-may-2026-core-update-rollout-is-now-complete-479119
- SER, mise à jour core de mai 2026 : https://www.seroundtable.com/google-may-2026-core-update-done-41435.html
- SER, mise à jour core de décembre 2025 : https://seroundtable.com/google-december-2025-core-update-completed-40671.html
- SEL, mise à jour core de juin 2025 : https://searchengineland.com/google-june-2025-core-update-rollout-is-now-complete-458617
- SEL, bilan 2025 : https://searchengineland.com/google-algorithm-updates-2025-in-review-3-core-updates-and-1-spam-update-466450
- SEL, bilan 2023 : https://searchengineland.com/google-algorithm-updates-2023-435732
- SEL, site reputation abuse et first-party (nov. 2024) : https://searchengineland.com/google-site-reputation-abuse-policy-now-includes-first-party-involvement-or-oversight-of-content-448432
- SEL, site reputation abuse et EEE (2026) : https://searchengineland.com/google-wont-respect-manual-actions-for-site-reputation-abuse-in-european-economic-area-486055
- SER, site reputation et EEE : https://www.seroundtable.com/google-site-reputation-policy-eea-41968.html
- SEJ, site reputation abuse : https://www.searchenginejournal.com/google-updates-site-reputation-abuse-policy-removes-penalties-in-eea/587423/
- PPC Land, spam update de septembre 2026 : https://ppc.land/googles-september-spam-update-ends-after-13-days-as-manual-actions-rise/
- GSQi, études de cas spam update 2026 : https://www.gsqi.com/marketing-blog/august-2026-google-spam-update-case-studies/
- Affiverse, impact sur les affiliés en mars 2026 (donnée JetDigitalPro) : https://www.affiversemedia.com/googles-march-2026-core-update-hit-affiliate-sites-harder-than-any-other-category/
- ALM Corp, analyse core update déc. 2025 : https://almcorp.com/blog/google-december-2025-core-update-complete-analysis-recovery-guide/
- PPC Land, récupération de HouseFresh : https://ppc.land/housefresh-achieves-notable-traffic-recovery-after-google-algorithm-impacts-2/
- Digital Applied, programmatique après mars 2026 : https://www.digitalapplied.com/blog/programmatic-seo-after-march-2026-surviving-scaled-content-ban
- Townsmith, scaled content et pages locales : https://townsmithwp.com/guides/scaled-content-recovery/

**IA dans la recherche, GEO**
- Abondance, lancement des AI Overviews en France : https://www.abondance.com/20260722-2640402-lancement-officielle-ai-overviews-france.html
- BDM, AI Overviews et AI Mode en France : https://www.blogdumoderateur.com/google-deploie-ai-overviews-ai-mode-france/
- SEL, recherches zéro clic en 2026 : https://searchengineland.com/google-zero-click-searches-2026-study-479717
- Press Gazette (Authoritas) : https://pressgazette.co.uk/media-audience-and-business-data/google-ai-overviews-publishers-report-clickthroughs-authoritas-report/
- TechWyse, étude randomisée sur l'AI Mode : https://www.techwyse.com/news/search-seo/google-ai-mode-reduces-publisher-clicks-study-2026
- Rexultz, AI Overviews et affiliation : https://rexultz.com/blog/ai-overviews-affiliate-sites-2026-data/
- GPTMelo, schémas de citation des plateformes IA : https://www.gptmelo.com/resources/ai-platform-citation-patterns-2026
- Agenzy, étude des sources citées : https://www.agenzy.lt/blog/which-sources-ai-engines-cite-2026

**Netlinking, domaines, technique, délais**
- SEJ, link spam update (liens d'affiliation et guest posts) : https://www.searchenginejournal.com/google-link-spam-update/
- NameSilo, évaluer un domaine expiré : https://www.namesilo.com/blog/en/domain-backorder/evaluating-expired-domains-history-links-and-risk
- Archivarix, domaines expirés : https://archivarix.com/en/blog/expired-domains/
- Bulkbase, expired domain abuse : https://bulkbase.ai/seo/expired-domain-abuse-googles-policy-examples-how-to-use-expired-domains-legitimately
- Ahrefs, combien de temps pour se classer : https://ahrefs.com/blog/how-long-does-it-take-to-rank/
- Ahrefs, Google Sandbox : https://ahrefs.com/blog/google-sandbox/
- SEJ, Core Web Vitals WordPress vs Astro : https://www.searchenginejournal.com/core-web-vitals-wordpress-and-astro/575818/
- Astro, rapport de performance des frameworks : https://astro.build/blog/2023-web-framework-performance-report

> **À revérifier régulièrement** : le Google Search Status Dashboard (dates des mises à jour), l'application de la politique site reputation abuse dans l'EEE, les CTR en présence d'AI Overviews en France (données post-juillet 2026 encore rares), et la confirmation d'une éventuelle core update de juillet 2026.
