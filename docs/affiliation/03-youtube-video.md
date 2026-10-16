# 03 — Affiliation via YouTube et vidéo courte

> Fiche de référence pour l'assistant IA. Rédigée le 16 octobre 2026.
> Légende utilisée partout : **[Fait]** = sourcé (lien en fin de fiche) · **[Estim.]** = estimation / chiffre déclaratif non vérifié · **[Avis]** = opinion ou recommandation de pratique · **[Incertain]** = sources contradictoires ou non officielles, à revérifier.

## Ce qu'il faut retenir

1. **YouTube = deuxième moteur et porte d'entrée dans Google.** Sur les requêtes d'achat ("avis X", "X alternative", "meilleur X", "X vs Y"), Google affiche souvent un bloc vidéo dominé par YouTube : une vidéo peut ranker là où un site neuf n'a aucune chance (banque, assurance, VPN, nutrition, dating). [Fait partiel / Avis]
2. **Le format roi en affiliation est le long format "décision"** (avis, comparatif, alternative, 4–10 min, chapitré), décliné en **Short "verdict" de 30–60 s** sur le même mot-clé. Les Shorts ne portent **aucun lien cliquable** dans la description ni les commentaires depuis le 31 août 2023 : ils servent de rabatteurs vers la vidéo longue (lien "vidéo associée") ou vers des tags Shopping. [Fait]
3. **Le risque n°1 est la démonétisation pour "contenu inauthentique"** (renommage du 15 juillet 2025 : contenu "répétitif ou produit en masse"). La règle vise les modèles, diaporamas, textes défilants et l'IA générique *sans perspective originale* — pas l'IA en soi. L'application se fait au niveau de la **chaîne entière**. Vague de fermetures en janvier 2026 (16 chaînes, ~4,7 Md de vues). [Fait]
4. **Pour l'affiliation pure, la démonétisation AdSense n'est pas fatale, mais la suppression/fermeture l'est.** Les liens d'affiliation sont autorisés ; ce qui est sanctionné, c'est le spam, le "malicious clickbait", la redirection hors plateforme comme *seul* objectif. [Fait]
5. **Divulgation obligatoire à deux niveaux** : case YouTube "contient une promotion payée" (contenu de marque) + droit français (loi n° 2023-451 du 9 juin 2023 : mention claire « Publicité » ou « Collaboration commerciale »). Pour un lien d'affiliation, mentionner explicitement « lien affilié » à l'oral et dans la description. [Fait / Avis sur l'application exacte aux liens affiliés]
6. **Contenu synthétique** : déclarer "AI use = Oui" seulement si c'est réaliste et trompeur (personne réelle, événement réel, scène réaliste, musique IA au premier plan). Script IA, miniature IA, infographies, **clonage de *sa propre* voix** : pas de déclaration requise. Une voix de synthèse "stock" n'est pas explicitement listée → [Incertain]. Déclarer n'affecte pas la monétisation. [Fait]
7. **YouTube Shopping affiliate est arrivé en France le 13 octobre 2026** (tags produits dans longs formats, Shorts et lives ; marchands type Amazon ; réservé aux chaînes YPP). Aux US, seuil abaissé à 500 abonnés (YPP élargi) le 27 mars 2026 ; Amazon intégré aux US le 27 août 2026. C'est la seule façon d'avoir un "lien" cliquable dans un Short. [Fait, relayé par la presse — à revérifier dans le Help Center FR]
8. **Pipeline faceless réaliste** : Claude Code → script → voix (ElevenLabs ou voix réelle) → animation par code (Remotion ou HyperFrames) → miniature depuis un "style JSON" → upload. Coût marginal faible (quelques € / vidéo), mais **la valeur doit venir d'un vrai test produit** (captures, chiffres, avis personnel), sinon risque inauthentique + faible conversion. [Fait pour les outils / Avis pour la stratégie]
9. **Multilingue** : le doublage automatique YouTube (27 langues revendiquées, ouvert largement en 2026) permet une chaîne unique multi-pistes ; mais pour l'affiliation, **une chaîne par langue** (FR, EN…) reste plus sûre pour titres/miniatures/liens localisés — c'est ce que fait Cybernews (chaînes FR, DE…). [Fait partiel / Avis]
10. **Veille** : `yt-dlp` (recherche `ytsearchN:`, métadonnées, chapitres, descriptions → liens affiliés des concurrents) + vidIQ (outliers, mots-clés, transcriptions). Repérer les **outliers** = vues ≫ abonnés et vidéos anciennes/peu vues sur des requêtes d'achat. [Avis / testé dans notre environnement]

---

## 1. Pourquoi YouTube pour l'affiliation

### 1.1 Le raisonnement de Franck (podcast "MVP", synthèse LinkedIn)
- Sa formation a été refondue **"YouTube d'abord, SEO ensuite"** ; il pousse ses élèves à faire les deux. [Fait — déclaratif]
- Niches où un site seul peine à ranker : **banque, assurance, parfois nutrition et dating** ; sur ces SERP, un bloc de 3 vidéos YouTube s'intercale entre Shopping et Maps. [Fait — déclaratif]
- Test cité (ChatSEO) : nom du concurrent + "avis" / "alternative", **1 vidéo horizontale FR + 1 EN + 1 Short résumé par vidéo** → page 1 à 4 endroits (YouTube FR, YouTube EN, Google FR, Google EN) d'après Ahrefs au moment de l'enregistrement. [Estim. — un seul cas, observation ponctuelle]
- Visage ou pas : les deux fonctionnent ; voix off sur slides Canva "largement suffisant" ; la plupart de ses meilleurs élèves ne se montrent pas. **Condition : sa propre voix, dans sa langue** (ElevenLabs peut cloner/traduire). [Avis]
- Sa chaîne test lancée le 4 juillet → première commission le 21 juillet (≈ 2–3 semaines). [Estim. — déclaratif]
- Garde-fou de l'auteur de l'article : *un agent peut monter, il ne peut pas avoir utilisé le produit à votre place*. Les formats qui durent montrent une vraie personne, de vrais tests, de vrais écrans. [Avis — partagé ici]
- Conflits d'intérêts déclarés dans l'article (ChatSEO sponsor, Wisewand outil de Franck). Le "20 k€/mois" du titre n'est pas vérifié.

### 1.2 Vidéos dans Google
- Données anciennes mais seules disponibles : analyse WSJ (2020) → **83 %** des vidéos des carrousels Google viennent de YouTube ; étude RankRanger → le 1er résultat du carrousel Google n'est en moyenne qu'en **position 14** dans la recherche YouTube ; Perficient → classements Google et YouTube différents **~64 %** du temps. [Fait — études datées, pas d'étude 2025-2026 trouvée]
- Conséquence pratique [Avis] : **optimiser pour Google ≠ optimiser pour YouTube**. Google lit titre, description, chapitres, transcription ; une petite chaîne peut apparaître dans le carrousel Google sans être top 5 sur YouTube.
- Avec les AI Overviews, les vidéos YouTube sont aussi citées comme sources ; pas de chiffre fiable trouvé. [Incertain]

### 1.3 Durée de vie
- Une vidéo "avis X 2026" peut convertir 12–24 mois, puis doit être **republiée** (nouvelle année, nouvelle version de produit). Les sources qui parlent de "revenus pendant des années" sont promotionnelles. [Estim./Avis]
- Avantage vs ads : personne ne "coupe" la chaîne du jour au lendemain… sauf YouTube lui-même (cf. §4). Franck préfère les canaux qu'on ne peut pas éteindre. [Avis]

---

## 2. SEO YouTube appliqué à l'affiliation

### 2.1 Recherche de mots-clés
Priorité aux **intentions d'achat** : `avis`, `test`, `alternative`, `vs`, `meilleur`, `prix`, `code promo`, `arnaque ?`, `ça vaut le coup ?`, `tuto` (post-achat, conversion forte sur outils SaaS).

Méthode [Avis] :
1. Lister offres + concurrents de l'annonceur (noms de marque).
2. Pour chaque marque : vérifier dans Google si un **bloc vidéo** apparaît (Ahrefs/Ubersuggest "SERP features" ou à la main).
3. Sur YouTube : `ytsearch20:"<marque> avis"` via yt-dlp → regarder âge des vidéos, vues, taille des chaînes. **Signal d'opportunité** : vidéos de plus de 12 mois, < 5 000 vues, petites chaînes, ou pas de vidéo en FR.
4. vidIQ `keyword_research` pour volume/concurrence YouTube.
5. Décliner en EN (et autres langues payantes : DE, ES, PT-BR, JP…) — Franck gagne surtout à l'international.

### 2.2 Titres
- Mot-clé exact **en début de titre** + promesse / tension : « NordVPN avis : ce qu'il faut VRAIMENT savoir avant de souscrire ». Ajouter l'année pour les requêtes saisonnières. [Avis]
- **Test & Compare** : depuis le 9 décembre 2025 (rollout global annoncé), test de jusqu'à 3 titres et/ou miniatures sur les longs formats, desktop, gagnant choisi sur la **part de temps de visionnage** (pas le CTR). Pas disponible pour les Shorts. [Fait — sources secondaires concordantes]
- Interdit : titres/miniatures "maliciously misleading" (politique spam, "Malicious clickbait"). Le "putaclic" assumé de Franck doit rester honnête sur le contenu. [Fait]

### 2.3 Description (modèle)
```
[Ligne 1-2, visible avant "plus"] : CTA + lien affilié + bénéfice (-XX %, essai gratuit…)
👉 Essayer <Produit> (lien affilié) : https://…
Divulgation : certains liens sont affiliés ; je touche une commission sans surcoût pour vous.

[Paragraphe SEO 80-150 mots : mot-clé principal + variantes + à qui s'adresse la vidéo]

Chapitres
00:00 Verdict en 30 secondes
00:30 Prix et offres
...
[Liens alternatives : Concurrent A (lien affilié), Concurrent B…]
[Lien vers l'article du site (maillage SEO ↔ YouTube)]
```
- Chapitres : premier horodatage obligatoirement `00:00` ; un chapitre = une idée ; titres de chapitres = sous-requêtes ("X est-il sûr ?", "X pour le streaming"). Observé chez Cybernews FR (vidéo NordVPN, 10 chapitres, lien affilié en 1re ligne, garantie 30 jours en 2e ligne). [Fait observé via yt-dlp]
- Liens en tête : recommandation de pratique (premiers ~200 caractères), pas d'étude de conversion trouvée. [Avis]

### 2.4 Placement des liens
| Emplacement | Long format | Short | Remarque |
|---|---|---|---|
| Description | Cliquable | **Non cliquable** depuis 31/08/2023 | Placer en ligne 1 |
| Commentaire épinglé | Cliquable | **Non cliquable** | Doublon du lien + question pour lancer l'engagement [Avis] |
| Fiches / cartes / écran de fin | Vers vidéos/playlists ; liens externes réservés aux YPP (sites associés) | — | [Incertain sur conditions actuelles] |
| Lien "vidéo associée" | — | 1 lien vers une vidéo de la chaîne | Pont Short → vidéo longue [Fait] |
| Liens de chaîne | Jusqu'à 12 liens près du bouton S'abonner | idem | [Fait] |
| Tags YouTube Shopping | Oui | **Oui** | Seul "lien produit" cliquable en Short ; YPP requis ; FR depuis 13/10/2026 [Fait] |

YouTube revendique **+110 % de clics produit** avec tags Shopping vs liens en description seuls (mesure 14–29 juillet 2026, chiffre YouTube non vérifié). [Fait — source YouTube relayée]

### 2.5 Miniatures, CTR, rétention
- Miniature = **logo/produit reconnaissable + verdict ou tension** (« ARNAQUE ? », note /10, "VS"), visage optionnel. Méthode Anthony/Franck : collecter 10–20 miniatures d'un style aimé → Claude produit un **style JSON** (palette, typo, composition, éléments) → réutilisé pour chaque miniature. [Avis]
- Rétention : donner le **verdict dans les 30 premières secondes** (les spectateurs en mode achat zappent sinon), puis justifier. Hook ≤ 15 s. [Avis]
- vidIQ `score_thumbnail` / `score_title` pour pré-tester, puis Test & Compare natif.

### 2.6 Structure d'une vidéo qui convertit (templates)

**A. "Avis <Produit>" (6–9 min)**
```
0:00 Hook + verdict court ("Je l'utilise depuis 3 mois : bon pour A, à éviter si B")
0:30 Pour qui / pour qui ce n'est pas (qualifie l'audience)
1:00 Prix réel, offres, pièges (renouvellement, engagement)
2:00 Démo écran : 3 usages concrets (preuves : captures, chiffres de test)
5:00 Points faibles (crédibilité = conversion)
6:00 Comparaison rapide avec 1-2 alternatives
7:00 Verdict final + CTA : "lien affilié en description, -XX % actuellement"
```
**B. "<Produit> alternative(s)" (5–8 min)** : pourquoi chercher une alternative (douleurs réelles du produit) → 3–5 alternatives, une par chapitre, chacune "meilleur pour…" → tableau récap à l'écran → recommandation n°1 + liens affiliés pour chacune.

**C. "<A> vs <B>"** : verdict immédiat par profil → 5 critères (prix, fonctionnalités, facilité, support, limites) avec écran partagé → "choisissez A si…, B si…" → liens des deux.

**D. Short "verdict" (30–45 s)** : même mot-clé dans le titre ; 0–3 s question ("NordVPN vaut-il le coup en 2026 ?") ; 3–30 s 3 arguments + 1 défaut ; fin : « test complet dans la vidéo liée » ; lien "vidéo associée" + tag Shopping si disponible.

### 2.7 Shorts vs long format pour l'affiliation
- Shorts jusqu'à **3 minutes** depuis le 15 octobre 2024 ; depuis le 31 mars 2025 une vue Short est comptée à chaque lecture/relecture (les "vues engagées" restent visibles dans Analytics). [Fait]
- Shorts = **découverte, volume, faible intention** ; long = **décision, conversion, rank Google**. Le Short ne vend pas seul (sauf tags Shopping). [Avis]
- Shorts : ~200 Md de vues/jour (lettre Neal Mohan, janv. 2026). [Fait — chiffre YouTube]

---

## 3. Chaînes "faceless" et automatisées

### 3.1 Stack
| Brique | Outils | Coût indicatif | Notes |
|---|---|---|---|
| Recherche & scripts | Claude Code + transcriptions concurrentes (yt-dlp/vidIQ) + notes de test réelles | abonnement | Le script doit intégrer **vos** observations |
| Voix | Votre voix (meilleur), ou ElevenLabs (clone de votre voix, traduction) | Starter ~5–6 $/mois (droits commerciaux), Creator ~22 $, Pro ~99 $ [Incertain : chiffres variables selon sources] | Version gratuite ElevenLabs non monétisable |
| Vidéo par code | **Remotion** (React) ou **HyperFrames** (HTML/CSS, HeyGen, Apache-2.0, sorti ~avril 2026) | Remotion gratuit pour individus et entreprises ≤ 3 salariés ; sinon "Automators" 0,01 $/rendu, min. 100 $/mois, "Creators" 25 $/siège/mois. HyperFrames : gratuit | HyperFrames : Node 22+ et FFmpeg, rendu déterministe Chrome headless |
| Captures/B-roll | Enregistrements d'écran réels du produit (OBS), stock, vidIQ `generate_broll` | 0–30 €/mois | Les captures réelles sont la meilleure preuve anti-"inauthentique" |
| Musique | Bibliothèque audio YouTube, vidIQ `generate_music` | 0 | Musique IA au premier plan = à déclarer |
| Miniatures | Modèle d'image + style JSON ; vidIQ `generate_thumbnail` | quelques centimes | Pas de déclaration IA requise |
| Upload/metadata | YouTube Studio ou API ; vidIQ `video_upload`, `update_video` | — | Cocher divulgations |

### 3.2 Pipeline proposé (Claude Code)
```
1. Choix sujet  : liste de ~10 "avis <X>" / "<X> alternative" par niche (opportunités §2.1)
2. Recherche    : yt-dlp → top 10 vidéos, chapitres, descriptions, transcriptions
                  + page de l'offre, prix, CGV, avis Trustpilot
3. Test réel    : l'humain utilise le produit, fait 5-10 captures + notes (NON automatisable)
4. Script       : Claude → template §2.6, verdict en ouverture, défauts inclus
5. Voix         : enregistrement perso ou clone ElevenLabs de SA voix (pas de voix stock générique)
6. Visuel       : Remotion/HyperFrames : composants réutilisables (tableau comparatif,
                  barre de note, prix, logo) + captures réelles insérées
7. Variantes    : Short 30-45 s (même composants, 9:16), version EN (voix traduite)
8. Miniature    : style JSON + logo produit + verdict
9. Métadonnées  : titre (3 variantes pour Test & Compare), description modèle, chapitres
10. Conformité  : checklist §4.6 → upload → lien "vidéo associée" sur le Short
11. Suivi       : clics affiliés (sub-ID par vidéo), Analytics à J+7/J+28
```
Coût marginal estimé : **2–10 € par vidéo** hors temps humain (voix + rendu + image). [Estim.]

### 3.3 Ce qui sépare une chaîne automatisée viable d'une chaîne démonétisée [Avis fondé sur la politique officielle]
- Chaque vidéo a **un angle et une information propre** (tests, chiffres, captures) — pas le même gabarit avec un nom de produit changé.
- Éviter : diaporamas d'images, texte défilant, narration générique, même structure + même conclusion sur 30 vidéos d'affilée.
- Rythme raisonnable (2–4 vidéos longues/semaine/chaîne plutôt que 3/jour).
- Varier : intros, formats (avis, vs, tuto, "après 6 mois"), durées.
- Rapports de presse : l'algorithme favoriserait les hôtes à l'écran et des faceless se font démonétiser en masse (témoignage Doctor NOS, 1,7 M abonnés, The Hollywood Reporter via TNW, juin 2026). Certains embauchent des présentateurs via Fiverr/Upwork. [Fait rapporté / Incertain sur l'algorithme]

---

## 4. Règles YouTube critiques (état au 16/10/2026)

### 4.1 Monétisation : "contenu inauthentique" et "contenu réutilisé"
- **15 juillet 2025** : la politique "repetitious content" est renommée **"inauthentic content"** et clarifiée : contenu **"répétitif ou produit en masse"**. La politique "reused content" n'a **pas** changé. [Fait — Help Center]
- Non autorisé (texte officiel) : contenu qui « semble fait avec un modèle », « diaporamas d'images, scénarios à gabarit, ou texte défilant avec peu ou pas de narration », contenu IA utilisant des modèles génériques **sans la perspective originale du créateur**, personnages remis dans la même situation avec la même issue. Autorisé : même intro/outro si le reste diffère ; séries/avis où chaque vidéo a son propre angle. [Fait]
- Contenu réutilisé : non autorisé sans commentaire original substantiel ; autorisé : extraits pour **critique**, réactions commentées. S'applique **même avec permission** et **à la chaîne entière**. [Fait]
- Ce n'est **pas une interdiction** de publier, c'est une exclusion du YPP (monétisation). [Fait]
- **Janvier 2026** : lettre annuelle de Neal Mohan → "gérer l'AI slop" est une priorité ; vague de **16 chaînes fermées** (~35 M abonnés, 4,7 Md vues, ~10 M$/an estimés). **Mars 2026** : test d'un sondage spectateur "est-ce de l'AI slop ?" (5 niveaux). [Fait — presse]
- Affirmations à **ignorer** : « 30 % de commentaire minimum », « YouTube a supprimé des millions de chaînes » — non présentes dans les politiques. [Fait — démenti par sources critiques]

### 4.2 Contenu synthétique ou modifié
- Déclaration dans Studio → section **Attributs → "AI use" (Oui/Non)**.
- **Obligatoire** si réaliste ET : personne réelle disant/faisant ce qu'elle n'a pas fait ; altération d'images d'un lieu/événement réel ; scène réaliste qui n'a pas eu lieu ; **musique IA au premier plan**.
- **Exempté** : contenu non réaliste/animé, retouches esthétiques, **aide à la production (plan, script, miniature, titre, infographie)**, sous-titres, amélioration audio/vidéo, **clonage de sa propre voix pour voix off ou doublage**, gameplay.
- Libellés : réaliste/musique → sur le lecteur ; audio IA non musical ou contenu animé → dans la description étendue. YouTube peut **étiqueter automatiquement** (outils YouTube, métadonnées C2PA, détection interne, SynthID) ; non modifiable pour Veo/Gemini, C2PA ou après revue manuelle.
- **La déclaration ne limite ni l'audience ni la monétisation** ; ne pas déclarer de façon répétée → libellé forcé, retrait, suspension du YPP. [Fait — Help Center]
- Pour nous : animations Remotion/HyperFrames + script IA + votre voix clonée → a priori "Non". Voix de synthèse générique ou avatar réaliste → déclarer "Oui" par prudence. [Avis / Incertain]

### 4.3 Spam, liens externes
- Politique "Spam, pratiques trompeuses et escroqueries" : couvre vidéos, descriptions, commentaires, lives, y compris les liens et les **URL obfusquées** ("point com" à l'oral compte comme lien). Interdit : "Off-platform diversion" = contenu créé **uniquement** pour envoyer hors YouTube ; "malicious clickbait" ; promotion de schémas "get rich quick" ; récompenses contre likes/abonnés. [Fait]
- Les liens d'affiliation ne sont pas une violation en soi ; le spam massif (mêmes commentaires, comptes dédiés) l'est. [Fait — sources secondaires sur la nuance]
- Prudence niches sensibles : finance/crypto/"argent facile", santé/compléments (allégations), contenus adultes (exclus de nombreux programmes et de la monétisation).

### 4.4 Divulgation des partenariats
- YouTube : **Studio → Détails → Promotion payée → "Ma vidéo contient du contenu de marque"** → libellé affiché au début de la vidéo. Le créateur est responsable du respect des lois ; YouTube renvoie vers la **DGCCRF** pour la France. La page ne mentionne pas explicitement l'affiliation. [Fait]
- France : **loi n° 2023-451 du 9 juin 2023** (JO du 10 juin 2023), art. 5 : mention « Publicité » ou « Collaboration commerciale » claire, lisible, identifiable sur la vidéo pendant toute la promotion ; usage des outils natifs des plateformes. Contrat écrit obligatoire au-delà d'un seuil (1 000 € HT annoncé par une source pour 2026 → [Incertain]). [Fait]
- Application aux liens affiliés seuls : **non tranché dans nos sources** → [Incertain]. Pratique recommandée [Avis] : cocher la case si l'annonceur fournit produit/rémunération fixe ; **toujours** dire « lien affilié » à l'oral + mention en description ; pour une audience US, règles FTC (divulgation claire et proche du lien).

### 4.5 Programme YouTube Shopping affiliate
- **US** : seuil abaissé de 10 000 abonnés à **YPP (y compris palier élargi, ≥ 500 abonnés)** le 27 mars 2026 ; 12 pays alors listés (US, KR, ID, TH, VN, MY, PH, IN, SG, BR, TW, JP). Exclus : chaînes musique/OAC, "conçu pour les enfants". Commission versée via AdSense **60 à 120 jours** après l'achat, annulée en cas de retour. [Fait — PPC Land citant la doc YouTube]
- **Royaume-Uni** : 6 août 2026 (6 marchands). **Amazon** dans le programme US : 27 août 2026 (catalogue sélectionné, auto-tagging, compte Amazon Associates/Influencer lié). [Fait — presse]
- **France : lancé le 13 octobre 2026** (YouTube Festival Paris) : tags produits dans vidéos, Shorts, lives ; marchands partenaires (ex. Amazon) ; YPP requis ; >1,3 M créateurs inscrits dans le monde ; valeur des ventes ×13 entre T1 2024 et T1 2026 (chiffres YouTube). [Fait — FashionNetwork, Siècle Digital, CapMad ; conditions exactes FR à vérifier dans Studio]
- Seuils YPP de référence : palier élargi 500 abonnés + 3 vidéos/90 j + 3 000 h/12 mois ou 3 M vues Shorts/90 j ; palier complet (pubs) 1 000 abonnés + 4 000 h ou 10 M vues Shorts/90 j. [Fait — à revérifier, seuils modifiables]
- **Limite** : catalogue grand public (e-commerce). Les offres SaaS/VPN/finance à forte commission restent en liens d'affiliation classiques.

### 4.6 Checklist de publication
- [ ] Mot-clé d'achat validé (bloc vidéo Google ? concurrence YouTube ?)
- [ ] Test réel du produit + captures propres (preuve d'originalité)
- [ ] Verdict dans les 30 premières secondes ; défauts mentionnés
- [ ] « Lien affilié » dit à l'oral + écrit en description
- [ ] Case « promotion payée » si contrat/produit offert ; mention « Publicité / Collaboration commerciale » à l'écran si collaboration (droit FR)
- [ ] Attribut « AI use » correctement renseigné
- [ ] Titre : mot-clé en tête ; 2–3 variantes en Test & Compare
- [ ] Description : lien + bénéfice en ligne 1 ; paragraphe SEO ; chapitres dès 00:00 ; lien vers l'article du site
- [ ] Commentaire épinglé avec lien + question
- [ ] Liens trackés par vidéo (sub-ID / tracker type Binom, Keitaro)
- [ ] Miniature conforme au style JSON, non trompeuse
- [ ] Short dérivé avec lien « vidéo associée » (+ tags Shopping si éligible)
- [ ] Pas de promesses illégales (santé, finance, « gains garantis »)
- [ ] Vérifier que la vidéo diffère réellement des 5 précédentes (structure, angle, visuels)

---

## 5. Multilingue

- **Doublage automatique** : lancé fin 2024 pour les chaînes "savoir" du YPP ; ouvert à tout le YPP vers avril 2025 ; plusieurs sources indiquent une ouverture à tous les créateurs le 4 février 2026 avec 27 langues et voix "expressives". **Lip-sync** annoncé au Made on YouTube (sept. 2025), encore en pilote limité. [Fait partiel / Incertain sur les dates exactes]
- **Pistes audio multiples** : vous uploadez vos propres doublages (ex. ElevenLabs avec votre voix clonée = exempté de déclaration). Titres/descriptions traduisibles ; miniatures multilingues signalées en 2026 [Incertain].
- **Une chaîne vs plusieurs** [Avis] :
  - *Une chaîne multi-pistes* : cumule l'autorité, simple ; mais liens affiliés et CTA restent uniques par description, le titre traduit n'est pas toujours optimisé, Google indexe mal les pistes doublées.
  - *Une chaîne par langue* : titres, miniatures, offres et liens **géolocalisés**, Shorts natifs ; meilleur pour l'affiliation. Exemple observé : **Cybernews** opère « Cybernews en Français » (~35 900 abonnés, oct. 2026) et « Cybernews Deutsch » avec des avis VPN par langue et liens affiliés en tête de description. [Fait observé]
  - Compromis : chaîne FR + chaîne EN (marché le plus large), autres langues via doublage auto pour tester la demande avant d'ouvrir une chaîne.
- Couplage tracker : router le clic selon pays/appareil vers la bonne offre (levier "le moins cher" selon Franck). [Avis]

---

## 6. Autres plateformes vidéo (bref)

- **TikTok Shop (France depuis le 31 mars 2025)** : affiliation créateur ≥ 18 ans, compte pro, **seuil cité 1 500 abonnés en France** (sources non officielles), compte Stripe, commissions ~5–20 %, versées ~15 jours après livraison ; échantillons gratuits des vendeurs. Fort sur produits physiques < 50 €, peu adapté au SaaS. [Fait partiel / Incertain sur seuils]
- **Instagram Reels** : tagging d'affiliation natif dans les Reels depuis le printemps 2026 (jusqu'à 30 produits/Reel, catalogue Meta), déploiement initial IN/US/BR/ID/TH — **pas confirmé pour la France**. Ailleurs : lien en bio / Stories. Le libellé "Partenariat rémunéré" ne suffit pas toujours juridiquement. [Fait — sources secondaires]
- **Pinterest** : liens affiliés autorisés sur les épingles (y compris vidéo) avec divulgation claire ; pas de masquage trompeur. Bon pour déco, cuisine, mode, DIY, trafic durable. [Fait — sources secondaires]
- Stratégie [Avis] : recycler le Short YouTube (9:16) vers TikTok/Reels, avec CTA adapté (pas de lien → "lien en bio", ou Shop tag).

---

## 7. Études de cas (ce qu'on sait vraiment)

Peu de chiffres audités existent ; la plupart des "income reports" faceless viennent de vendeurs de formations/outils. [Fait — constat]

| Cas | Données | Fiabilité |
|---|---|---|
| Franck (podcast MVP) | Chaîne test 04/07 → 1re commission 21/07 ; formation "YouTube first" | Déclaratif |
| Test ChatSEO | 4 positions page 1 (YT FR/EN, Google FR/EN) sur le nom d'un concurrent avec 2 vidéos + 2 Shorts | Observation ponctuelle |
| Cybernews (VPN, multi-langues) | Chaînes par langue ; vidéo « Avis sur NordVPN » FR : ~31 800 vues, 10 chapitres, lien affilié ligne 1 (yt-dlp, oct. 2026) | Observé, revenus inconnus |
| Micode « NordVPN vous ment (non sponsorisé) » | ~2,2 M vues sur la même requête → l'angle critique/indépendant capte l'attention | Observé ; non affilié |
| "SaaS Breakdown" (avis logiciels, 412 K abonnés) | 22–45 K$/mois estimés, comparatifs "HubSpot vs Salesforce" | Estimation d'un vendeur |
| Chaîne faceless (Medium) | 12 758 $ en avril 2025 dont 3 880 $ affiliation | Déclaratif, auteur vend un cours |
| 16 chaînes fermées janv. 2026 | 35 M abonnés, 4,7 Md vues | Presse ; illustre le risque |

Leçon [Avis] : sur une requête d'avis, **les gros succès sont des angles incarnés** (test, critique, enquête), les vidéos génériques plafonnent à quelques milliers de vues mais peuvent convertir car l'intention est forte.

---

## 8. Outillage dans notre environnement : veille concurrentielle

### 8.1 yt-dlp (testé le 16/10/2026, v2026.08.19)
- **OK** : recherche, métadonnées, chapitres, descriptions. **Téléchargement vidéo bloqué (403 datacenter)**. Les sous-titres peuvent échouer avec « Sign in to confirm you're not a bot » (observé) → réessayer plus tard ou basculer sur vidIQ `video_transcript`.
- Avertissement attendu : pas de runtime JS (deno) → certaines métadonnées peuvent manquer.

```bash
# 1. Lister les 30 vidéos qui rankent sur une requête d'achat
yt-dlp "ytsearch30:nordvpn avis" --flat-playlist \
  --print "%(id)s|%(title)s|%(view_count)s|%(channel)s|%(duration)s" > serp.tsv

# 2. Métadonnées complètes (date, abonnés, chapitres, description = liens affiliés)
yt-dlp --skip-download --print \
  "%(id)s|%(upload_date)s|%(view_count)s|%(channel_follower_count)s|%(like_count)s|%(comment_count)s" \
  -a ids.txt
yt-dlp --skip-download -J "https://www.youtube.com/watch?v=ID" > meta.json   # .chapters, .description, .tags

# 3. Sous-titres auto (transcription pour analyser la structure du script)
yt-dlp --skip-download --write-auto-subs --sub-langs "fr.*,en.*" --sub-format vtt -o "%(id)s" URL

# 4. Toutes les vidéos d'une chaîne concurrente (sans téléchargement)
yt-dlp --flat-playlist --print "%(id)s|%(title)s|%(view_count)s" "https://www.youtube.com/@cybernewsfr/videos"
```

### 8.2 Analyses à automatiser (Claude Code)
- **Outlier score** = vues / abonnés de la chaîne (ou / médiane des vues de la chaîne). > 3 = sujet ou angle qui sur-performe → à étudier.
- **Opportunité SERP** : sur les 10 premiers résultats, compter vidéos > 12 mois, < 5 K vues, absence de FR → score.
- **Extraction des liens affiliés** dans les descriptions (regex sur domaines de redirection : `cnews.link`, `go.`, `?ref=`, `aff_id`, `awin`, `impact`…) → identifie les programmes et les promos qui convertissent dans la niche.
- **Structure des chapitres** des 5 meilleures vidéos → plan de script (sous-requêtes à couvrir).
- **Transcriptions** → hooks des 30 premières secondes, objections traitées, CTA, durée avant le 1er CTA.

### 8.3 vidIQ (connecteur MCP)
- `vidiq_keyword_research` (volume/compétition YouTube), `vidiq_outliers` et `vidiq_similar_videos` (sujets qui sur-performent), `vidiq_youtube_search`, `vidiq_channel_videos` / `vidiq_channel_stats` (concurrents), `vidiq_video_transcript` (repli quand yt-dlp est bloqué), `vidiq_video_comments` / `comment_insights` (objections et questions → nouvelles vidéos), `vidiq_score_title` / `score_thumbnail`, `vidiq_generate_video_chapters`, `vidiq_trending_videos`, `vidiq_instagram_tiktok_outlier_search` (veille Reels/TikTok).
- Production possible (`generate_script`, `voiceover_generate`, `generate_thumbnail`, `video_upload`) — à utiliser comme assistance, pas comme usine à gabarits (§4.1). Vérifier les crédits (`vidiq_balance`).

### 8.4 Routine de veille hebdomadaire proposée [Avis]
1. Pour chaque niche : 10 requêtes d'achat × `ytsearch30` → tableau SERP.
2. Calcul outliers + opportunités → top 5 sujets.
3. Transcriptions + chapitres des 3 meilleures vidéos par sujet → brief.
4. Commentaires des vidéos concurrentes → questions non traitées.
5. Mise à jour de la liste de production (§3.2).

---

## 9. Points incertains à revérifier régulièrement
- Conditions exactes de YouTube Shopping affiliate **en France** (seuil, marchands, commission).
- Application de la loi influenceurs aux **liens d'affiliation seuls** (sans contrat) — avis DGCCRF/ARPP.
- Voix de synthèse "stock" : déclaration IA requise ou non.
- Dates précises du doublage automatique pour tous et des miniatures multilingues.
- Conditions actuelles des liens externes dans les fiches/écrans de fin.
- Tarifs ElevenLabs (crédits/caractères variables selon les sources).
- Remotion 5.0 annonce un changement de licence.

---

## Sources

**Article de départ**
- LinkedIn — « Affiliation SEO : la machine à 20k€/mois de Franck » : https://fr.linkedin.com/pulse/affiliation-seo-la-machine-%C3%A0-20kmois-de-franck-avec-claude-vengeons-rq2we

**YouTube officiel (Help Center)**
- Politiques de monétisation YouTube (inauthentic / reused content, mise à jour 15/07/2025) : https://support.google.com/youtube/answer/1311392
- Divulgation du contenu altéré ou synthétique : https://support.google.com/youtube/answer/14328491
- Promotions payées / contenu de marque : https://support.google.com/youtube/answer/154235
- Spam, pratiques trompeuses et escroqueries : https://support.google.com/youtube/answer/2801973
- Politique relative aux liens externes : https://support.google.com/youtube/answer/9054257
- Shorts (durée, comptage des vues) : https://support.google.com/youtube/answer/10059070

**Politique inauthentique / AI slop**
- Plagiarism Today (juil. 2025) : https://www.plagiarismtoday.com/2025/07/08/youtube-targets-inauthentic-content/
- Gulf News (15/07/2025) : https://gulfnews.com/technology/youtube-updates-monetisation-policies-ai-and-repetitive-content-ban-begins-july-15-1.500192660
- TNW (15/06/2026) : https://thenextweb.com/news/youtube-ai-slop-crackdown-faceless-creators-collateral-damage
- Variety AU — lettre Neal Mohan 2026 : https://au.variety.com/2026/digital/global/youtube-channels-using-ai-tools-reduce-slop-neal-mohan-letter-32190/
- RightsTech (janv. 2026) : https://rightstech.com/2026/01/youtube-chief-says-managing-ai-slop-is-a-priority-for-2026/
- YTGrowth (démêler vraies/fausses règles) : https://ytgrowth.io/blog/youtube-ai-policy

**Contenu synthétique (secondaire)**
- TechCrunch (2024) : https://techcrunch.com/?p=2680198
- MiniMatters : https://minimatters.com/youtube-altered-or-synthetic-content-disclosure/

**Liens Shorts et YouTube Shopping**
- Tubefilter (liens Shorts, 2023) : https://tubefilter.com/2023/08/10/youtube-shorts-comments-spam/
- Search Engine Journal (liens Shorts) : https://www.searchenginejournal.com/youtube-adds-shorts-links-limits-links-elsewhere/495463
- PPC Land — Shopping affiliate à 500 abonnés (27/03/2026) : https://ppc.land/youtube-opens-shopping-affiliate-program-to-creators-with-500-subscribers/
- PPC Land — Royaume-Uni : https://ppc.land/youtube-opens-shopping-affiliate-program-to-uk-creators-with-six-retailers/
- Social Media Today — Amazon : https://www.socialmediatoday.com/news/youtube-adds-amazon-affiliate-links/829031/
- FashionNetwork FR (France, oct. 2026) : https://fr.fashionnetwork.com/news/Youtube-deploie-son-programme-d-affiliation-youtube-shopping-en-france,1875843.html
- Siècle Digital (13/10/2026) : https://siecledigital.fr/2026/10/13/youtube-shopping-arrive-en-france-et-ouvre-un-nouveau-marche-aux-createurs-de-contenu/
- CapMad : https://www.capmad.com/post/on-13-october-youtube-shopping-lands-in-france-and-turns-videos-into-affiliate-storefronts
- vidIQ — guide YouTube Shopping : https://vidiq.com/blog/post/youtube-shopping/

**SEO YouTube / Google**
- Search Engine Land (YouTube dans les résultats vidéo Google) : https://searchengineland.com/youtube-remains-dominant-source-of-video-in-top-google-ranking-positions-344458
- Pure SEO (écarts YouTube vs Google) : https://pureseo.com/us/blog/google-blog/study-finds-disparity-between-youtube-google-video-rankings
- SEJ — Title A/B testing : https://www.searchenginejournal.com/youtube-title-a-b-testing-rolls-out-globally-to-creators/562571/
- vidIQ — Title testing : https://vidiq.com/blog/post/youtube-launches-new-title-testing-tool/
- PPC Land — comptage vues Shorts : https://ppc.land/youtube-changes-how-shorts-views-are-counted-from-march-31/
- Social Media Today — Shorts 3 min : https://www.socialmediatoday.com/news/youtube-expands-3-minute-shorts-to-all-users/736967/
- Metricool — horodatages : https://metricool.com/add-timestamps-youtube/

**Multilingue**
- TechSpot — lip-sync : https://www.techspot.com/news/109532-youtube-introduces-ai-lip-syncing-auto-dubbing-videos.html
- Metricool — doublage auto : https://metricool.com/youtube-multi-language-audio-tracks-now-available-for-more-creators/
- BeMultilingual (2026) : https://www.bemultilingual.ca/blog/youtube-dubbing-updates

**Outils**
- Remotion — pricing : https://www.remotion.dev/docs/license/pricing
- HyperFrames — GitHub : https://github.com/heygen-com/hyperframes ; docs : https://hyperframes.heygen.com/introduction
- ElevenLabs tarifs (secondaire) : https://bigvu.tv/blog/elevenlabs-pricing-2026-plan-worth/ ; https://www.hackceleration.com/labs/elevenlabs-pricing

**Droit français**
- Ministère de l'Économie — loi influenceurs : https://www.economie.gouv.fr/node/3222759
- Université de Lille — blog juridique influenceurs : https://master-droitdeladistribution.univ-lille.fr/fileadmin/user_upload/master-droitdeladistribution/Documents/BLOG_JURIDIQUE_INFLUENCEURS.pdf

**Autres plateformes**
- TikTok Shop affiliation (secondaire) : https://www.formalive.fr/affiliation-tiktok-shop/ ; https://www.valueyournetwork.com/createurs-tiktok-shop-france/
- Instagram Reels affiliate : https://metricool.com/instagram-reels-affiliate-links/ ; Ballard Spahr (mai 2026) : https://www.ballardspahr.com/insights/alerts-and-articles/2026/05/tag-you-are-liable-what-instagrams-new-affiliate-reels-mean-for-retailers
- Pinterest affiliate (secondaire) : https://pingenerator.com/blog/pinterest-affiliate-links-policy

**Études de cas (fiabilité faible, vendeurs)**
- SaaS Breakdown : https://aivideoempire.com/case-studies/saas-breakdown
- Medium — faceless dashboard : https://medium.com/@connect.najibsir/inside-our-faceless-channel-dashboard-real-income-revealed-8aaba514b26f
- Observations directes yt-dlp (16/10/2026) : https://www.youtube.com/watch?v=IjK4hAd2tbc ; https://www.youtube.com/watch?v=ckZGQ5cLIfs
