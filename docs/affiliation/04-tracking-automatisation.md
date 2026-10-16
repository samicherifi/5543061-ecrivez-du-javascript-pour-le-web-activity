# 04 — Tracking, analytics, trafic payant et automatisation IA en affiliation

> Fiche de référence (mémoire durable) pour accompagner un entrepreneur francophone en affiliation SEO + YouTube (France et international).
> Rédigée le 16 octobre 2026. Point de départ : l'article LinkedIn de Paul Vengeons (12 oct. 2026) qui résume l'épisode #146 du podcast **MVP** (Paul Vengeons et Antoine Veyrieres) avec **Franck** (Franck Marc, cofondateur de Wisewand), enregistré en juillet 2026.
>
> **Légende.** **[FAIT]** : vérifié dans une source citée. **[DÉCLARATIF]** : chiffre ou affirmation d'une personne, non vérifiée. **[ESTIMATION]** : ordre de grandeur, à revérifier. **[OPINION]** : jugement de l'auteur cité ou de cette fiche. **[INCERTAIN]** : les sources se contredisent ou sont secondaires.

---

## Ce qu'il faut retenir

1. **Un tracker se place entre le clic et l'offre.** Il enregistre la source (page, vidéo, pays, appareil) et choisit la destination. D'après Franck, c'est le levier le plus rentable qu'il ait ignoré pendant des années : « +30 à 50 % de CA » **[DÉCLARATIF, de mémoire]**. Sur un site 100 % français avec une offre française, le gain peut être proche de zéro (Vengeons).
2. **Le gain vient surtout du routage par pays, pour éviter le « fallback »** des plateformes (l'offre de repli, souvent mauvaise, montrée aux visiteurs hors du pays principal). Le routage par appareil est de la micro-optimisation, à faire seulement si des données de conversion le justifient.
3. **Il faut une boucle complète : lien avec sub-ID, puis postback S2S.** Sans postback serveur, le tracker compte les clics mais pas les ventes. Il faut donc toujours passer un click ID dans le paramètre sub-ID du réseau.
4. **Choix de l'outil.** Pour démarrer, des liens propres avec UTM/sub-ID par page et par vidéo suffisent (Pretty Links, Lasso, ou un Cloudflare Worker maison). Binom ou Keitaro (auto-hébergés, environ 40 à 105 €/$ par mois) deviennent utiles une fois qu'on a du trafic multi-pays. Hyros est un outil d'attribution du parcours d'achat (pour vendre son propre produit), pas un routeur d'affiliation.
5. **Les redirections sont permises, à condition de rester transparentes.** Mettre `rel="sponsored"` sur les liens affiliés. Ne jamais montrer à Google autre chose qu'au visiteur (cloaking). Pour Amazon : ne jamais masquer le site référent ni rendre la destination Amazon floue.
6. **Mesurer le revenu par page, pas le trafic.** Joindre Search Console (requêtes et clics par page), les clics sortants GA4 ou du tracker, et les commissions (postbacks) pour obtenir l'EPC et le RPM par page. En France, GA4 reste soumis au consentement CNIL **[FAIT, sources secondaires concordantes]**.
7. **Le trafic payant (Meta, Google, Pinterest, native) marche si 1 € investi rapporte plus de 1 €.** Mais un bannissement de compte coupe tout du jour au lendemain. C'est pour cela que Franck privilégie SEO et YouTube **[OPINION de Franck]**.
8. **Claude Code automatise autour de la page** : briefs, migrations, maillage, audits, rapports, règles de tracker. La règle d'or : l'IA n'utilise que les données qu'on lui colle ou qui viennent d'un MCP, elle marque `[MANQUANT]` ou `[BESOIN DE MOI]`, et un humain valide avant toute mise en ligne.
9. **Les risques Google sont réels.** Scaled content abuse, expired domain abuse et spam de liens (PBN) sont des politiques explicites (page mise à jour le 28/08/2026), avec de nombreuses spam updates en 2026 (mars, juin, août, septembre). Pas de programmatique sur un domaine neuf. Le PBN automatisé de Franck reste **son** risque.
10. **L'ordre pour partir de zéro** : offre → requêtes d'achat → vidéo YouTube + Short avec lien tracké → site simple et lent → 5 liens internes par page → attendre environ 3 mois → routage tracker → scale. Compter de façon réaliste 3 à 9 mois avant un revenu régulier **[ESTIMATION]**.

---

## 1. Ce que dit la source (article Vengeons / épisode MVP avec Franck)

**Contexte [FAIT, d'après l'article].** Franck fait de l'affiliation depuis 2012-2013. Il a monté à Malte, avec trois associés, une structure qui ne faisait que des sites affiliés (« plusieurs millions de commissions » **[DÉCLARATIF]**). Aujourd'hui, il gère ses propres sites, Wisewand (outil de rédaction IA, cofondé avec Arthur et Anthony, avec API, CLI et MCP), un podcast et une académie. L'épisode #146 s'intitule « 20k/mois avec le business de l'affiliation automatique ».

**Chiffres cités, tous déclaratifs.** Un site à 288 000 clics en 28 jours (niche adulte, difficilement reproductible). « Plein » de sites entre 10 000 et 60 000 clics/mois. Marge de 50 % minimum, souvent 70 à 80 %. Revente d'un site à 2 000 €/mois pour 40 000 à 60 000 €. Domaine expiré hors enchères à environ 10 €. Sites du PBN à 100-200 clics/jour, certains au-delà de 1 000. Tracker : +30 à 50 %. Première commission de sa chaîne YouTube perso environ 2-3 semaines après le lancement du 4 juillet 2026.

**Ce que Franck fait vraiment (selon ses propos) :**
- Tous ses projets sont dans **Claude Code cloud connecté à GitHub**. Les articles sont planifiés avec Claude, rédigés par Wisewand (via son MCP), mis en file, puis **GitHub Actions publie une page par jour**.
- Il refait les « sites fatigués » : nouveau template, migration WordPress vers **Astro** ou **WordPress headless**, puis un article par jour.
- Il fait tourner un **PBN sur domaines expirés**, nourri sans humain par une base de contenus, avec un article par jour par site. Il a obtenu une vue unique du trafic de tous ses sites en demandant à Claude branché sur le **MCP Ahrefs**.
- Côté tracker, il utilise **Binom** et cite **Maxconv** et **Keitaro**. Pour leur formation, ils utilisent **Hyros** (parcours YouTube → LinkedIn → podcast → achat), branché à leur tableau de bord par API.
- Il revoit ses « flows » (règles de routage) tous les 1 à 2 mois : d'où vient le trafic, s'il existe un partenaire spécialisé sur ce pays, quelle offre convertit par marché et par appareil.
- Sur l'automatisation : « Je fais encore des trucs un peu à la papa ». Il n'utilise pas d'agents qui achètent des domaines tout seuls (cite Hermes comme exemple chez d'autres).

**Mises en garde de l'auteur [FAIT].** Les prompts ont été écrits pour l'article et ne sont pas testés. Les chiffres sont oraux. Personne n'est neutre (ChatSEO sponsor, SEO Monkey agence d'Antoine, Wisewand outil de Franck, lien affilié Wisewand de l'auteur).

---

## 2. Tracking d'affiliation

### 2.1 Le mécanisme de base

```
Visiteur ──clic──> lien "propre" (ex. monsite.com/go/offre-x?src=page-slug)
            └──> TRACKER : enregistre click_id, page/vidéo, pays, appareil, langue, heure
                   └──> applique les règles (flow) ──302──> URL de l'offre + &subid={click_id}
                          └──> l'annonceur/le réseau conserve le subid
                                 └──> vente ──postback S2S──> tracker?cid={click_id}&payout=12.50
```

- **Sub-ID** : un paramètre que le réseau accepte et renvoie (`subid`, `sub1`, `aff_sub`, `clickref`, `tag` selon les plateformes). On y met un click ID unique, ou au minimum `page-slug` ou `video-id`. La syntaxe des macros varie (`{clickid}`, `${sub1}`, `#s2#`…). **Toujours vérifier la doc du réseau** [FAIT, AnyTrack, Voluum, ClickFlare].
- **Postback S2S** : quand la conversion a lieu, le serveur du réseau appelle l'URL du tracker avec le click ID et souvent le montant et le statut. Ce mécanisme ne dépend ni des cookies du navigateur ni des bloqueurs de pubs [FAIT]. Il faut le tester avec une conversion test avant d'envoyer du trafic. Certains réseaux d'affiliation grand public n'offrent pas de postback. Dans ce cas, on importe des rapports CSV par sub-ID.
- **Routage (flow / stream / path)** : les règles sont évaluées de haut en bas. Exemple : offre par défaut → règle par pays → éventuellement par appareil, langue du navigateur ou opérateur.
- **Smartlink** : un seul lien qui choisit automatiquement l'offre selon le profil du visiteur. Certains réseaux en fournissent un « clé en main » ; c'est justement là que se cache le fallback décrit par Franck.
- **A/B test d'offres** : répartir le trafic (50/50, ou pondéré) entre deux offres ou deux landers dans une même règle. On compare l'**EPC** (revenu / clics) et non le taux de conversion seul. Il faut un volume suffisant : avec 200 clics par variante et un taux de conversion de 2 %, l'écart n'est pas significatif **[ESTIMATION]**. Laisser tourner au moins 2 à 4 semaines (le délai de validation des commissions peut aller de 30 à 90 jours selon les programmes).

### 2.2 Éviter le fallback (le gain que Franck décrit)

Le problème : 80 % des visiteurs d'un site anglophone viennent des États-Unis et tombent sur la bonne offre. Les 20 % restants (UK, Inde, Allemagne…) tombent sur l'offre de repli de la plateforme, « souvent claquée », alors qu'une autre plateforme est peut-être spécialisée sur ce pays.

Méthode de vérification (Vengeons) :
1. Analytics : visiteurs par pays sur 3 mois.
2. Additionner la part hors du pays ciblé par l'offre principale : c'est le trafic qui part en fallback.
3. Demander à la plateforme ce que voient les visiteurs de ces pays.
4. Ne poser de règles par appareil que si les données de conversion le montrent.

Cas Amazon : **OneLink** (gratuit) redirige les visiteurs vers leur boutique Amazon locale, en remplaçant le tag par le tag lié du pays. Cela suppose d'être inscrit au programme Partenaires de chaque pays. Les raccourcisseurs tiers ne sont pas pris en charge [FAIT, aide Amazon ; liste des pays **INCERTAINE**, à vérifier dans Associates Central].

### 2.3 Cloaking, redirections et conformité

| Pratique | Statut |
|---|---|
| Lien `/go/xxx` en 301/302 vers l'offre, même destination pour Google et l'humain | OK. Les redirections légitimes sont autorisées par Google |
| `rel="sponsored"` (ou `nofollow`) sur les liens affiliés | **Demandé par Google** pour les liens affiliés, qu'ils soient manuels ou dynamiques. Manque = risque d'action manuelle ou algorithmique |
| `Disallow: /go/` dans robots.txt | Pratique courante **[OPINION]**. Ce n'est pas une obligation |
| Montrer un contenu à Googlebot et un autre au visiteur (« cloaking ») | **Interdit** (politique spam Google). Sur Meta, c'est un motif de bannissement immédiat |
| Redirection « sneaky » vers un contenu inattendu | **Interdit** |
| Amazon : raccourcisseur qui rend la destination Amazon floue, ou redirections qui masquent le site référent | **Interdit** par le contrat Partenaires (formulations citées par des tiers, **à vérifier dans le texte officiel en vigueur**). `amzn.to` et les liens complets sont OK |
| Cookie stuffing, faux clics, auto-achats, bots, enchères sur la marque sans autorisation, codes promo non autorisés | **Fraude ou violation**. Ne jamais faire ni aider à faire |

**Mentions légales.** En France, la loi n° 2023-451 du 9 juin 2023 impose une mention claire « Publicité » ou « Collaboration commerciale » à toute personne qui, à titre onéreux, promeut des biens ou services. La DGCCRF contrôle et sanctionne [FAIT]. L'application aux liens affiliés d'un YouTuber est une **interprétation prudente** : la rémunération à la commission est onéreuse, donc il vaut mieux mentionner. Aux États-Unis, la FTC exige une divulgation claire, à l'oral dans la vidéo et à côté des liens. Une étude ICWSM 2026 portant sur environ 2 millions de vidéos montre que la plupart ne respectent pas ces règles [FAIT].

### 2.4 Comparatif des trackers (prix 2026, **à revérifier** chez l'éditeur)

| Outil | Modèle | Prix indicatif | Pour qui | Notes |
|---|---|---|---|---|
| **Binom** | Auto-hébergé (v2) ou Cloud | v2 ≈ 104 $/mois. Cloud de 49 à 299 $ selon les sources. Module Protect ≈ 69 $ **[INCERTAIN]** | Affilié solo avec du volume, utilisé par Franck | Très rapide, rétention longue en self-hosted. Demande un VPS |
| **Keitaro** | Auto-hébergé | ≈ 40 / 72 / 104 €/mois (Starter / Advanced / Expert) + VPS ≈ 30 $. Essai 14 jours | Bon rapport qualité-prix, pas de limite d'événements | Admin API sur Expert. Il existe des MCP communautaires (non officiels) |
| **Voluum** | SaaS cloud | ≈ 99 à 149 $/mois en entrée + dépassement ≈ 0,05-0,06 $ / 1 000 événements | Media buyers, grosses intégrations | Cher au volume |
| **RedTrack** | SaaS | ≈ 69-149 $ en entrée, jusqu'à ≈ 1 000 $. L'offre « AI Team » inclut un MCP **[INCERTAIN]** | Pub payante + e-commerce, sync des régies | Plafonds d'événements |
| **MaxConv** | SaaS | Offre gratuite ≈ 150 000 événements/mois, 3 mois de rétention, 25 campagnes **[source forum AffLift]** | Débutant, test | Peu de documentation indépendante |
| **Hyros** | SaaS d'attribution | Sur devis, ≈ 200-380 $/mois minimum, échelonné selon le revenu suivi, appel commercial obligatoire | Vendre **son propre** produit (formation) | Ce n'est pas un routeur de liens d'affiliation |
| **Pretty Links / Lasso** | Plugins WordPress | Pretty Links : version gratuite + payante. Lasso ≈ 190 $/an **[INCERTAIN]** | Site WordPress débutant | Liens propres, alertes de liens cassés ou ruptures de stock (Lasso). Peu de routage |
| **Cloudflare Worker maison** | Code (edge) | Offre gratuite généreuse (vérifier les quotas) | Développeur JS, site Astro | Géo via `request.cf.country`. Logs à construire soi-même |

Exemple minimal de Worker (routage pays + sub-ID + log). Ce n'est pas un tracker complet : il ne reçoit pas de postback sans code supplémentaire.

```js
// worker.js — /go/:slug  → offre selon le pays
const OFFERS = {
  "vpn-x": { default: "https://network-a.example/off?id=1", DE: "https://network-b.example/de?id=9" },
};
export default {
  async fetch(req, env) {
    const url = new URL(req.url);
    const slug = url.pathname.split("/")[2];
    const o = OFFERS[slug];
    if (!o) return new Response("Not found", { status: 404 });
    const country = req.cf?.country || "XX";
    const clickId = crypto.randomUUID();
    const dest = new URL(o[country] || o.default);
    dest.searchParams.set("subid", `${url.searchParams.get("src") || "na"}_${clickId}`);
    // env.CLICKS = binding KV/D1/Analytics Engine pour journaliser {clickId, slug, country, ua, src, ts}
    return Response.redirect(dest.toString(), 302);
  },
};
```

Point d'attention : la carte d'exemple de Cloudflare utilise la clé `EU`, alors que `request.cf.country` renvoie des codes ISO pays. Il faut donc lister chaque pays.

### 2.5 Tracking côté YouTube

- **Un lien par vidéo et par emplacement** : `monsite.com/go/offre?src=yt-<videoId>-desc`, `…-pin` (commentaire épinglé), `…-short`. Ajouter les UTM **avant** le raccourcissement.
- Préférer un **domaine à soi** (`/go/`) aux raccourcisseurs génériques : on peut changer l'offre sans modifier 200 descriptions, et c'est plus lisible.
- Côté Amazon : lien complet ou `amzn.to` (pas de raccourcisseur tiers qui masque la destination). On peut créer plusieurs tracking IDs Amazon (un par chaîne ou par vidéo) pour mesurer.
- Divulgation : à l'oral au début et par écrit à côté du lien. Le réglage « promotion payée » de YouTube ne remplace pas la divulgation.
- Les commissions d'une vidéo arrivent souvent avec un décalage. Il faut juger une vidéo sur 60 à 90 jours **[ESTIMATION]**.

---

## 3. Analytics

### 3.1 Search Console et son API
- La **source de vérité SEO** : requêtes, pages, clics, impressions, position, par pays et appareil. Le rapport **Pages** (indexation) permet de voir les « explorée/détectée, actuellement non indexée », signe que Google a vu la page et l'a écartée.
- **API Search Analytics** : depuis avril 2025, Google propose des données horaires sur 10 jours (dimension `HOUR`, dataState `HOURLY_ALL`) [FAIT, blog Google]. Les quotas (environ 1 200 requêtes/min par site, jusqu'à 50 000 lignes par requête avec pagination) sont **[INCERTAIN]** : les sources tierces divergent, vérifier la doc officielle. Les derniers jours sont provisoires : à chaque import, recharger une fenêtre glissante de 3 à 4 jours.
- Usage typique avec Claude Code : un script (Python ou Node) exporte chaque semaine `page × requête × pays` en CSV ou SQLite, puis Claude classe et commente.

### 3.2 GA4
- Activer les **mesures améliorées > clics sortants** : l'événement `click` est alors envoyé avec `link_url`. On peut aussi créer un événement `affiliate_click` quand `link_url` contient le domaine `/go/` ou celui du réseau, avec `page_path` en paramètre [FAIT, guides Analytify/AnyTrack].
- GA4 ne voit pas la commission. Elle arrive dans le réseau ou le tracker. Il faut faire la jointure par sub-ID ou par page.

### 3.3 EPC et RPM par page (le vrai tableau de bord)
- **EPC (earnings per click)** = commissions / clics sortants sur l'offre.
- **RPM page** = commissions / sessions (ou clics Search Console) × 1 000.
- **CTR affilié** = clics sortants / sessions de la page.
- Construction : `Search Console (page → clics)` + `tracker ou GA4 (src=page → clics sortants)` + `réseau ou postback (subid=page → commissions validées)`. Une page à fort trafic et à RPM proche de zéro est souvent une page « apprend/perdu ». Une page à faible trafic mais à RPM élevé est à pousser (liens internes, mise à jour).

### 3.4 Consentement (France / UE)
- **GA4 n'entre pas dans l'exemption CNIL** de mesure d'audience dans sa configuration standard. Il faut donc un bandeau de consentement [FAIT, sources secondaires concordantes : Cookiebot, Dotsland]. La CNIL a précisé l'exemption par une délibération de juillet 2025 (finalité strictement limitée, données anonymes).
- **Consent Mode v2** est obligatoire pour les annonceurs Google ciblant l'EEE depuis mars 2024. Il **ne remplace pas** le bandeau. Le mode basic n'envoie rien sans consentement, le mode advanced envoie des pings sans cookies. Évolutions annoncées en juin 2026 : **[INCERTAIN]**.
- Alternatives exemptables (Matomo configuré, et quelques autres solutions listées par la CNIL) pour garder une mesure de base sans consentement. Le tracker de redirection côté serveur (logs du `/go/`) n'utilise pas de cookie navigateur. Il reste soumis au RGPD (IP = donnée personnelle) : minimiser, tronquer les IP et fixer une durée de conservation **[OPINION / vérifier avec un juriste]**.

---

## 4. Trafic payant en affiliation (arbitrage)

**Principe.** On achète un clic (Meta, Google Ads, Pinterest, Taboola/Outbrain/MGID pour le native, push), on l'envoie vers une page « pré-lander » puis vers l'offre, et on garde la marge `EPC - CPC`. Ici le tracker est **indispensable** : il sert à couper une source déficitaire en quelques heures.

**Avis de Franck [OPINION, épisode] :**
- Meta est devenu plus compliqué pour l'affiliation. Ça marche encore sur des produits chers. Franck lui-même n'y est pas retourné « depuis très longtemps ». Autrefois, 1 € rapportait 3-4 €, parfois 10-15 € **[DÉCLARATIF]**.
- Google Ads : les coûts sont très variables, on peut beaucoup dépenser pour peu de retour. Pinterest Ads : possible sur des niches très précises. LinkedIn : trop cher.
- Raison principale : **le jour où le compte pub est banni, tout s'arrête**. SEO et YouTube sont des actifs que personne ne peut éteindre du jour au lendemain.
- Sa règle : « Du moment que tu peux mettre 1 € et ressortir avec du bénéfice, go ».

**Risques documentés (2025-2026) :**
- **Meta** : de nombreux rapports de vagues de bannissements en 2026, liés à des comportements opérationnels (scripts qui modifient beaucoup d'annonces d'un coup, incohérences de paiement ou d'IP), au cloaking (bannissement immédiat) et aux promesses de revenus ou de santé. Les bannissements s'étendent aux comptes liés **[sources vendeurs, INCERTAIN quant aux chiffres]**.
- **Google Ads** : la politique « Insufficient original content » refuse les pages dont le seul but est de renvoyer vers un autre site (bridge pages, doorways) [FAIT, aide Google Ads]. Une page affiliée doit apporter une vraie valeur.
- **Économie** : le CPC monte avec la concurrence. Les commissions sont validées tardivement ou annulées (retours, fraude), alors que l'on paie le clic tout de suite. Il faut de la trésorerie et des tests à perte. Beaucoup de programmes **interdisent** le paid search sur la marque ou certaines sources : lire les conditions avant toute campagne.

**Recommandation pour cet entrepreneur [OPINION].** Ne pas faire de payant tant que l'on n'a pas une offre dont l'EPC organique est connu. Ensuite, faire un test borné (budget perdu accepté, par exemple 200-300 €), une source à la fois, avec tracker et postback. Pinterest ou YouTube Ads vers ses propres vidéos d'avis sont souvent moins risqués que du direct-linking.

---

## 5. Automatisation avec Claude Code appliquée à l'affiliation

### 5.1 Architecture recommandée

```
repo-site/                      (Astro ou WP headless, déployé via Cloudflare Pages/Netlify/Vercel)
├── CLAUDE.md                   règles permanentes du site (voir ci-dessous)
├── .claude/skills/
│   ├── brief-article/SKILL.md  produire un brief depuis les données GSC/Ahrefs/Ubersuggest
│   ├── publier-page/SKILL.md   checklist "une page par exécution"
│   ├── maillage/SKILL.md       proposer 5 liens internes entrants
│   ├── audit-declin/SKILL.md   pages qui perdent du trafic
│   └── flows-tracker/SKILL.md  règles pays/appareil
├── content/queue/*.md          file d'attente (statut: pret | BESOIN_DE_MOI)
├── data/                       exports GSC, tracker, réseau (CSV/SQLite, hors git si sensibles)
├── scripts/gsc_export.py       API Search Console
└── .github/workflows/publish.yml  cron quotidien → publie 1 page "pret"
```

- **CLAUDE.md** : niche, offres et pays acceptés, ton, template de page, règles de publication (ci-dessous), pages protégées, interdictions (pas de commission ni d'avis inventés, pas de test fictif).
- **MCP utiles** : Search Console (connecteurs communautaires ou scripts maison), Ahrefs (le serveur MCP officiel distant serait sorti début 2026 selon un tiers, setup piégeux entre 2 serveurs et 2 types de clés, à partir d'environ 129 $/mois **[INCERTAIN]**), Ubersuggest (dispo dans cet environnement, demande une autorisation OAuth), vidIQ (recherche de mots-clés YouTube, outliers, transcriptions), Wisewand (MCP), éventuellement l'API ou un MCP du tracker (Keitaro : MCP communautaires non officiels, RedTrack : MCP sur l'offre haute).
- **Exécution planifiée** :
  - **GitHub Actions** avec `anthropics/claude-code-action@v1` en mode automation (`schedule: cron`, en UTC) [FAIT, doc officielle Claude Code].
  - **Routines Claude Code cloud** (research preview depuis avril 2026, intervalle minimum de 1 h, déclencheurs schedule/API/GitHub, chargent CLAUDE.md et `.claude/skills/` du repo) **[sources tierces]**.
  - **Scheduled tasks** de session ou desktop.
  - Penser au coût : les budgets par tâche sont peu documentés.

### 5.2 Règles permanentes (à coller dans CLAUDE.md, d'après Vengeons, adaptées)

```
RÈGLES DE PUBLICATION (à lire avant chaque nouvelle page)
1. Une seule nouvelle page par exécution, même si la file est longue.
2. Lister les pages existantes ; si une page vise déjà cette requête, s'arrêter et le signaler.
3. La requête visée en premier dans le title, mot pour mot.
4. Utiliser le template enregistré ; ne rien redessiner.
5. Ajouter 5 liens internes VERS la nouvelle page depuis des pages de même thématique (ancre = mot-clé).
6. Données structurées, auteur + bio, ajout au sitemap ; liens affiliés en /go/... avec rel="sponsored".
7. Tout ce qui exige une expérience réelle (test, chiffre, capture) = [BESOIN DE MOI] ; la page reste en file.
8. Après publication : vérifier HTTP 200, bon title, présence dans le sitemap ; rapport en une ligne.
9. Ne jamais modifier une page publiée depuis < 90 jours sans demande explicite.
10. N'inventer aucune commission, offre, avis client ou résultat de test.
```

### 5.3 Workflows concrets et prompts types

**a) Tri des requêtes et quick wins (hebdomadaire)**
> « Voici mes requêtes Search Console sur 3 mois (requête, page, clics, impressions, position) et ce que je vends. N'utilise que ces données. Classe chaque requête en ACHÈTE / APPREND / PERDU. Donne la part des clics par catégorie. Liste les ACHÈTE en position 5-20 avec la page positionnée. Regroupe-les par pattern (avis, alternative, prix, A vs B) et liste les pages manquantes évidentes. Toute idée absente des données doit porter la mention [IDÉE, VOLUME À VÉRIFIER]. »

**b) Brief d'article (skill `brief-article`)** : SERP actuelle (via MCP Ahrefs/Ubersuggest ou capture collée), blocs présents (vidéo, shopping, AI Overview), intention, 5 points à couvrir, l'élément que « seul quelqu'un qui a utilisé le produit saurait » (sinon `[À REMPLIR PAR MOI]`), emplacement de l'offre, 5 pages sources pour le maillage.

**c) Rédaction assistée + relecture humaine** : le premier jet est fait par l'IA (Claude ou Wisewand), puis un humain ajoute ses tests, captures et avis, puis Claude fait une vérification (faits, liens, schema, divulgation). On ne publie jamais une page encore marquée `[BESOIN DE MOI]`.

**d) Migration / refonte de template** (prompt de Vengeons, résumé) : inventaire des URL, title, H1, canonical et liens entrants. Les pages qui ont eu au moins 1 clic sur 3 mois sont **PROTÉGÉES** (même URL, title, H1, contenu principal). Plan de redirections en un seul saut. Nouveau template testé sur UNE page, puis attente du feu vert. Vérifications après migration : redirections sans chaîne, sitemap, schema, hreflang, maillage. Prévoir environ 90 jours de transition.

**e) Maillage interne automatique** : à chaque nouvelle page, Claude cherche (grep ou embeddings) les 5 pages les plus proches et propose une phrase et une ancre dans chacune. Le résultat est soumis en PR GitHub, pas en commit direct.

**f) Audit des pages en déclin (mensuel)**
> « Compare les clics par page sur les 28 derniers jours et sur la même période de l'an dernier (ou les 28 jours précédents). Liste les pages à -30 % ou pire avec ≥ 100 clics avant. Pour chacune, donne les requêtes perdues, l'évolution de position, si la SERP a changé (vidéo, AI Overview, forum), la date de dernière mise à jour, et le RPM. Propose : mettre à jour, fusionner, ou laisser. Ne propose aucune réécriture d'une page modifiée il y a moins de 90 jours. »

**g) Veille YouTube** : `yt-dlp --flat-playlist --dump-json https://www.youtube.com/@concurrent/videos` donne un JSON par vidéo (certains champs comme la durée ou les vues peuvent manquer). Avec un fichier archive, on ne détecte que les nouveautés. Alternative : l'API YouTube Data (quota) ou le MCP vidIQ (outliers, mots-clés, transcriptions). Respecter les CGU de YouTube et rester sur un volume raisonnable.

**h) Flows tracker (tous les 1-2 mois)** (prompt de Vengeons, résumé) : visiteurs par pays et appareil, offres et pays acceptés, autres plateformes, ventes par pays. Pour chaque pays au-dessus de 2 % : bonne offre, fallback ou rien. Estimer la part en fallback avec le calcul détaillé. Écrire les règles (défaut → pays → appareil si justifié). Lister les pays sans offre. Définir les mesures à suivre pendant 30 jours. « Ne promets aucun gain, n'invente aucune offre ».

**i) Rapport hebdomadaire (scheduled task, lundi)** : clics GSC (semaine contre semaine précédente), top 10 pages par RPM, nouvelles pages indexées ou non, clics sortants et commissions par page et par vidéo, alertes (lien cassé, offre en rupture, chute de plus de 30 %). Sortie : une page Markdown ou un ticket GitHub.

**j) Audit global (prompt « unique » de Vengeons)** : 8 contrôles notés OK / FAIBLE / MANQUANT (modèle, canaux, format SERP, mots-clés d'achat, liens, publication/indexation, programmatique, flows), puis les 3 contrôles qui coûtent le plus, un plan semaine/mois, et la liste des exports manquants.

### 5.4 Ce qui est risqué (faire la part des choses)

| Usage | Niveau de risque |
|---|---|
| Analyse de données, briefs, audits, migrations validées, maillage en PR, rapports | Faible : c'est le meilleur retour sur investissement de l'IA |
| Rédaction IA + vraie expérience humaine + rythme modéré (1 à 2 pages/semaine sur site neuf, environ 1/jour sur site établi) | Modéré, acceptable |
| Pages programmatiques (template × ville/produit) sur un domaine neuf | **Élevé** : « soufflé » selon Franck. Vengeons dit avoir perdu des impressions après la spam update de mars 2026 |
| Publication 100 % autopilote sans relecture, à volume élevé | **Élevé** : scaled content abuse, qu'il y ait de l'IA, des humains ou les deux |
| PBN automatisé sur domaines expirés | **Élevé et explicitement contraire** aux politiques (spam de liens, abus de domaines expirés). Franck l'assume, ce n'est pas une recommandation |
| Pages affiliées qui recopient les fiches marchand | Contraire à la politique « thin affiliation » |

---

## 6. Plan d'action « de zéro au premier revenu »

D'après l'ordre de Franck et Vengeons. Les délais sont des **[ESTIMATIONS]** réalistes pour une personne seule à temps partiel.

| Étape | Contenu | Jalon / délai |
|---|---|---|
| **1. Offre** | Une seule offre qu'on recommanderait de toute façon. Vérifier la commission, la durée du cookie, les pays acceptés, les sources autorisées et l'existence d'un postback ou de sub-IDs | Semaine 1 : offre validée, compte affilié actif |
| **2. Requêtes d'achat** | « [produit] avis », « alternative », « prix », « A vs B ». Analyser la SERP de chacune (bloc vidéo ? AI Overview ? forums ?) | Semaine 1-2 : 20-30 requêtes priorisées |
| **3. Vidéo** | Si un bloc vidéo contient de vieilles vidéos, commencer par là : 1 vidéo horizontale + 1 Short, avec sa voix et un vrai test | Semaines 2-4 : 2-4 vidéos. Première commission possible en 2-8 semaines, sans garantie |
| **4. Lien tracké dès le jour 1** | `/go/offre?src=yt-<id>` (Worker ou plugin), sub-ID transmis au réseau, divulgation | En même temps que l'étape 3 |
| **5. Site simple** | Astro ou WordPress léger, une page parfaite faite à la main, puis un template. Environ 1 page/semaine sur domaine neuf (Vengeons). GSC branchée, `rel="sponsored"`, mentions légales, bandeau cookies | Mois 1-2 : 5-10 pages |
| **6. Liens internes** | 5 liens entrants par page depuis des pages de même thématique | À chaque publication |
| **7. Attendre** | Ne pas juger une page avant environ 3 mois. Après une publication, passer au mot-clé suivant au lieu de retoucher | Mois 3-4 : premières positions et premières ventes SEO |
| **8. Tracker et flows** | Dès qu'il y a ≥ 10-15 % de trafic hors du pays principal ou ≥ 2 offres : Binom/Keitaro ou Worker, routage pays, postback, puis A/B test d'offres | Mois 3-6 |
| **9. Scale** | Seulement ensuite : versions EN (dossier `/en/` sur un domaine non lié à un pays), deuxième site, netlinking, programmatique sur domaine établi, payant en test borné | Mois 6+ |

**Repères pour décider [OPINION].** Si après environ 6 mois on a des pages indexées et classées, mais un RPM proche de zéro, le problème est l'offre ou l'intention, pas la quantité de contenu. Si le taux d'indexation est faible (beaucoup de « explorée, actuellement non indexée »), il faut ralentir et améliorer, pas publier plus.

**Routine hebdomadaire proposée par Vengeons** : lundi audit global, mardi SERP des 10 mots-clés principaux, mercredi tri GSC, jeudi pays des visiteurs, vendredi vidéo d'avis + Short. Revoir les flows tous les deux mois.

---

## 7. Points incertains / à vérifier régulièrement
- Les prix des trackers (fortes divergences selon les sources et entre USD et EUR) et ceux de Hyros (sur devis).
- Le texte exact actuel du contrat Amazon Partenaires (raccourcisseurs, redirections) et la liste des pays OneLink.
- Les quotas de l'API Search Console. Le statut et le prix du MCP Ahrefs officiel.
- Les changements de Consent Mode v2 annoncés en juin 2026 et les contrôles CNIL 2026 (sources : blogs).
- La portée exacte des spam updates d'août et de septembre 2026 (Google n'a pas tout détaillé).
- Tous les chiffres de Franck (déclaratifs, de mémoire, conflits d'intérêts déclarés).

---

## Sources

- Paul Vengeons, « Affiliation SEO : la machine à 20k€/mois de Franck, automatisée avec Claude Code », LinkedIn, 12/10/2026 — https://fr.linkedin.com/pulse/affiliation-seo-la-machine-%C3%A0-20kmois-de-franck-avec-claude-vengeons-rq2we
- Podcast MVP (Antoine Veyrieres, Paul Vengeons) — https://podcasters.spotify.com/pod/show/minimumviablepodcast-mvp · https://podcasts.apple.com/fr/podcast/mvp-le-podcast-seo-geo/id1698730807 · https://www.blogdumoderateur.com/mvp-podcast-seo-geo/
- Franck Marc (LinkedIn) — https://fr.linkedin.com/in/franck-marc · Avis Wisewand 2026 (secondaire) — https://agence404.com/outils-seo/wisewand/ · https://creator-economy.org/wisewand-review/
- Google, Politiques anti-spam (MAJ 28/08/2026) — https://developers.google.com/search/docs/essentials/spam-policies
- Spam updates 2026 (secondaires) — https://www.seo-kreativ.de/en/blog/google-march-2026-spam-update/ · https://www.digitalapplied.com/blog/google-june-2026-spam-update-rollout-site-owner-guide · https://www.egochi.com/blog/google-september-2026-spam-update/ · https://ppc.land/scaled-content-abuse/
- rel="sponsored" et liens affiliés — https://ppc.land/google-asks-publishers-to-label-affiliate-links · https://success.awin.com/articles/en_US/Knowledge/How-to-Add-the-Sponsored-Link-Attribute-to-Affiliate-Links
- Google Ads, Insufficient original content — https://support.google.com/adspolicy/answer/16427718
- Search Analytics API, données horaires (avril 2025) — https://developers.google.com/search/blog/2025/04/san-hourly-data · quotas (tiers) — https://serpview.com/blog/search-console-api-limits
- Postback S2S — https://doc.voluum.com/en/tracking_conversions_postback.html · https://anytrack.io/blog/postback-url/ · https://help.clickflare.com/en/tracking/tracking-conversions-using-s2s-postback
- Comparatifs trackers 2026 — https://remoby.com/blog/best-affiliate-tracking-software-2026/ · https://bigbetty.io/news/keitaro-vs-binom-vs-voluum-which-tracker-wins-for-igaming-affiliates/ · https://360uniquizer.com/en/news/trackers-keitaro-binom-redtrack-2026 · https://voluum.com/blog/voluum-pricing/ (éditeur)
- MaxConv (forum) — https://afflift.com/f/threads/%F0%9F%94%B5-how-to-start-with-maxconv-tracker.14810/page-2
- Hyros pricing (tiers) — https://costbench.com/software/marketing-attribution/hyros/ · https://usermaven.com/blog/hyros-pricing
- Keitaro MCP communautaire — https://glama.ai/mcp/servers/KeitaroManager/keitaro-mcp
- Lasso / Pretty Links — https://www.capterra.com.sg/compare/220053/1018745/pretty-link/vs/lasso · https://getlasso.co/best-affiliate-link-plugins-2/
- Cloudflare Workers, country code redirect — https://developers.cloudflare.com/workers/examples/country-code-redirect/
- Amazon : liens raccourcis / cloaking (citations tierces) — https://geniuslink.com/blog/link-cloaking-amazon/ · https://conductatlas.com/platform/amazon-associates/amazon-associates-operating-agreement/special-links-requirement/ · OneLink — https://affiliate-program.amazon.com/help/node/topic/GAGAL4V362SH7EC5
- GA4 et clics affiliés — https://analytify.io/track-affiliate-links-with-ga4/ · https://anytrack.io/playbooks/track-affiliate-commissions-in-ga4
- CNIL / consentement — https://www.cookiebot.com/fr/google-analytics-rgpd-2/ · https://www.quantic-avocats.com/2025/10/03/deliberationcnilcookiesaudience/ · https://dotsland.com/en/audience-measurement-without-consent/
- Loi influenceurs 2023 — https://www.lagbd.org/Influenceur_sur_les_reseaux_sociaux_et_la_Loi_du_9_juin_2023 · https://www.economie.gouv.fr/node/3222759
- YouTube, affiliation et FTC — https://ojs.aaai.org/index.php/ICWSM/article/view/42748 · https://entreresource.com/youtube-affiliate-marketing/
- Meta, bannissements 2026 (sources vendeurs) — https://affiliatevalley.com/news/metas-2026-crackdown-why-mass-bans-and-stricter-algorithms-are-catching-advertisers-off-guard/ · https://www.stackmatix.com/blog/meta-ads-policy
- Ahrefs MCP (tiers) — https://studiomeyer.io/en/blog/ahrefs-mcp-server-setup · https://seoprofy.com/blog/best-mcp-server-for-seo/
- Claude Code GitHub Actions (officiel) — https://code.claude.com/docs/en/github-actions · Routines / scheduled tasks (tiers) — https://makerkit.dev/blog/tutorials/claude-code-routines-guide · https://www.alexdunlop.com/writing/claude-code-scheduled-tasks
- yt-dlp playlists — https://www.mintlify.com/yt-dlp/yt-dlp/guides/playlists
