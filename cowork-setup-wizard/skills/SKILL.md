---
name: cowork-setup-wizard
description: >
  Setup personnel de 2 à 3 minutes pour un·e employé·e BOLEAN qui démarre sur
  Cowork. Produit un court texte de préférences à coller dans Cowork
  Settings → Preferences. Aucune écriture sur le Drive partagé, aucun dossier
  de travail créé, aucun fichier before/after persisté. Utiliser quand un·e
  employé·e BOLEAN dit « set up cowork », « configure cowork », « personalize
  cowork », « make cowork know me », « cowork feels generic », ou lors de
  l'onboarding d'un·e nouvel·le arrivant·e. À lancer une fois au premier
  démarrage Cowork de chaque membre de l'équipe.
---

# BOLEAN — Cowork Setup Wizard

**Ton rôle :** tu aides un·e employé·e BOLEAN à produire un texte de préférences personnelles à coller dans Cowork Settings → Preferences. Tu ne crées pas de dossiers, tu n'écris rien sur le Drive partagé, tu ne fabriques pas de fichier before/after. Tu produis **un seul texte**, stocké en scratchpad dans le dossier outputs de la session pour copier-coller.

**Durée cible :** 2 à 3 minutes. **Trois questions.**

**Ton de l'interaction :** direct, concis. Les employé·e·s BOLEAN sont occupé·e·s ; ce skill doit livrer vite et sans cérémonie.

---

## Architecture — règles non négociables

- **Contexte agence** (périmètre autorisé, conventions, architecture des dossiers clients) : dans `AI/00_AGENCE/`, maintenu par l'équipe. **Déjà en place pour toute l'équipe.** Ne pas le recréer, ne pas le dupliquer, ne pas y écrire depuis ce skill.
- **Préférences personnelles** : à coller dans **Cowork Settings → Preferences**. **Jamais** sur le Drive partagé. Les stocker en scratchpad dans `outputs/` pour copier-coller.
- **Hors-périmètre (« off-limits »)** : règle agence définie dans `AI/00_AGENCE/00_CONTEXTE.md` (seul `AI` est autorisé). Ne **pas** reposer la question à chaque employé·e. C'est une règle d'équipe, pas une préférence individuelle.
- **Dossier de travail personnel** : NE PAS en créer. Chaque employé·e organise son travail comme iel le veut.
- **Exemple before/after** : si l'employé·e le demande, le montrer en chat. Ne pas le sauvegarder.

---

## Déroulé

### Étape 1 — Présenter

Dire :

> « On met en place Cowork pour toi en 3 questions. À la fin, je te donne un court texte à coller dans Cowork Settings → Preferences. Rien n'est écrit sur le Drive partagé — c'est personnel. Environ 3 minutes. »

### Étape 2 — Vérifier que le socle agence existe

Vérifier la présence de `AI/00_AGENCE/00_CONTEXTE.md`.

- **Si présent** : continuer. C'est ce fichier que les préférences personnelles pointeront.
- **Si absent** : **ne pas le créer depuis ce skill.** Dire à l'employé·e : « Le socle agence `AI/00_AGENCE/00_CONTEXTE.md` n'est pas en place. C'est un travail d'équipe, pas un setup individuel. Signale-le à l'équipe qui maintient le socle. On peut continuer ton setup personnel, mais tes préférences pointeront vers un fichier qui n'existe pas encore. »

### Étape 3 — Trois questions (une à la fois, attendre chaque réponse)

**Q1 — Rôle et activités :**
> « Ton rôle chez BOLEAN, et les 3 activités sur lesquelles tu passes le plus de temps ? »

**Q2 — Style de communication + exemples concrets :**
> « Comment tu aimes recevoir l'info — concis / détaillé, formel / décontracté ? Donne-moi un exemple d'une phrase que tu trouverais bien tournée, et un exemple d'une phrase que tu trouverais lourde ou agaçante. »

Insister pour obtenir les deux exemples concrets. Sans eux, le style reste vague et les préférences n'ont pas d'effet opérationnel. Si l'employé·e sèche, proposer un exemple et demander à le valider ou le modifier.

**Q3 — Outils métier :**
> « Tes outils quotidiens en plus des outils partagés BOLEAN (Gmail, Google Chat, Calendar, Drive, Asana, Freshbooks) ? »

### Étape 4 — Produire le texte

Écrire dans `outputs/<prenom>-preferences-a-coller.md` un texte en première personne, structuré ainsi :

```markdown
# À coller dans Cowork Settings → Preferences (tout ce qui est sous la ligne).
# Ne pas sauvegarder ce fichier sur le Drive partagé — il est personnel à <prenom>.

---

Je suis [rôle] chez BOLEAN. Mon travail :
- [activité 1, dans leurs mots]
- [activité 2, dans leurs mots]
- [activité 3, dans leurs mots]

Style de communication attendu : [longueur + ton, dans leurs mots].
Exemple de bonne phrase : « [exemple fourni Q2] »
Exemple à éviter : « [contre-exemple fourni Q2] »

Outils spécifiques à mon rôle : [liste Q3].

Contexte agence : lire `AI/00_AGENCE/00_CONTEXTE.md` au démarrage de toute tâche cliente. Ce fichier contient le périmètre autorisé, l'architecture des dossiers clients, et les conventions BOLEAN. Ne pas dupliquer son contenu ici.
```

Contraintes sur ce texte :
- **Écrit en français.** Le Drive et les clients sont en français.
- **Moins de 250 mots.** Au-delà, Cowork Settings devient illisible et l'effet se dilue.
- **Rien de transitoire.** Pas d'objectifs « les 2 prochaines semaines », pas de projet en cours — ça périme, ça pollue.
- **Pas de duplication avec `00_AGENCE/`.** Outils partagés, périmètre, conventions → pointés, pas copiés.
- **Les mots de l'employé·e.** Pas de reformulation marketing, pas de broderie.

### Étape 5 — Livrer

Dire :

> « C'est prêt : `outputs/<prenom>-preferences-a-coller.md`.
>
> Marche à suivre (environ 30 secondes) :
> 1. Ouvrir Cowork Settings → Preferences.
> 2. Copier tout ce qui est sous la ligne de séparation dans le fichier.
> 3. Coller, enregistrer.
>
> À partir de la prochaine session, Cowork aura ce contexte en tête sans que tu aies à le rappeler. Si tu veux voir la différence avant/après, dis-le-moi et je te montre la même demande traitée avec et sans — en chat, pas en fichier. »

---

## Checks avant de conclure

- [ ] 3 questions posées. Pas de 4ème. Pas de sous-question parasite.
- [ ] Q2 a bien collecté **un exemple positif ET un exemple négatif concrets**.
- [ ] Texte rédigé en français, en première personne, avec les mots de l'employé·e.
- [ ] Texte sous 250 mots.
- [ ] Aucun fichier créé sur le Drive partagé `AI/`.
- [ ] Aucun dossier de travail personnel créé.
- [ ] Aucune règle hors-périmètre répétée dans le texte (elle est dans `00_AGENCE/`).
- [ ] Aucun objectif transitoire (« ce mois-ci », « ce trimestre ») dans le texte.

---

## Dépannage

**Cowork reste générique après avoir collé ?**
Vérifier que tout le texte sous la ligne a bien été collé (pas seulement le premier paragraphe), et que l'enregistrement a eu lieu. Redémarrer la session Cowork.

**Pas d'accès à Cowork Settings → Preferences ?**
Chercher « Personalization », « User Context », ou « À propos de toi ». Si vraiment absent, coller le texte en début de chaque nouvelle session comme palliatif.

**L'employé·e demande un dossier de travail personnel créé par le skill ?**
Décliner. Lui expliquer que le skill ne crée pas de dossier — iel organise son travail comme iel veut, et pas sur le Drive partagé `AI/` (qui est réservé au contenu agence et clients).

**`AI/00_AGENCE/00_CONTEXTE.md` absent ?**
Ne pas le créer depuis ce skill. C'est une tâche d'équipe. Avertir l'employé·e et continuer son setup personnel en pointant vers ce chemin futur.

---

## Skills liés (si présents)

- `/kickoff-client` — crée un nouveau dossier client depuis `_TEMPLATE/`.
