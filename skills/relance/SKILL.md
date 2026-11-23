---
name: relance
description: "Utilise CE skill DÈS QUE l'utilisateur doit relancer quelqu'un qui ne répond pas : il dit « relance », « fais-moi une relance », « il ne m'a pas répondu », « je n'ai pas de nouvelles de… », « le devis est parti il y a dix jours », ou colle un échange resté sans réponse (devis, proposition, facture, candidature, rendez-vous à caler), même sans demande explicite. Écrit la relance prête à envoyer, adaptée au canal (mail, SMS, WhatsApp, LinkedIn) et au rang de la relance (première, deuxième, dernière), sans jamais inventer un fait. Apprend le ton de l'utilisateur à partir d'une relance qu'il a aimée."
allowed-tools: Read, Write, Edit
---

# /relance : quelqu'un ne répond pas, la relance part en une minute

## Pour quoi faire

**Entrée** : la situation, dite comme on la raconterait : « devis de 2 400 € envoyé le 3 à Mme
Laurent pour la cuisine, pas de nouvelles », ou l'échange collé tel quel, ou un fichier du dossier
(le devis, le mail envoyé).
**Sortie** : **la relance prête à copier**, au bon ton pour le bon canal, plus une version courte,
et le moment conseillé pour la suivante.

L'effet magique : la relance qu'on repousse depuis trois jours, parce qu'on ne sait pas comment
la tourner sans avoir l'air d'insister, est écrite en une minute, et elle sonne comme vous.

## Aucune dépendance

Ce skill ne dépend d'aucun outil externe, il marche immédiatement. Il **n'envoie rien** : il
écrit, la personne copie et envoie elle-même.

## Comment procéder

> *(Instructions pour toi, le skill. « Tu » = toi qui exécutes. « Vous » = la personne qui t'a
> lancé.)*

### Étape 1. Lire la mémoire du skill

Regarde si `mon-ton.md` existe **dans le dossier de ce skill** (le dossier qui contient ce
`SKILL.md`). S'il existe, lis-le : c'est la façon d'écrire de la personne (tutoiement ou
vouvoiement, longueur, formule d'ouverture, signature, mots qu'elle emploie ou évite). Tu
l'appliques sans le redemander. S'il n'existe pas, tu écris avec un ton par défaut : poli,
direct, chaleureux, court.

### Étape 2. Rassembler les faits, sans en inventer un seul

Cherche dans cet ordre, et **ne redemande pas ce qui est déjà dit** :
1. la demande elle-même et la conversation en cours ;
2. un fichier que la personne a cité ou collé (devis, mail, proposition) : lis-le ;
3. le `CLAUDE.md` du projet, s'il dit ce que fait la personne.

Les faits dont la relance a besoin :
- **qui** on relance (prénom, nom ou société, et le lien : client, prospect, partenaire, recruteur) ;
- **quoi** est resté sans réponse (un devis, une proposition, une facture, une candidature, une date
  de rendez-vous, une question) ;
- **depuis quand** (la date d'envoi, ou « il y a deux semaines ») ;
- **le canal** de la relance (mail par défaut, ou bien SMS, WhatsApp ou LinkedIn si la personne le dit
  ou si l'échange d'origine s'y trouvait) ;
- **le rang** : première relance, deuxième, ou dernière. Si l'historique montre déjà une relance
  restée sans réponse, c'est la deuxième. Deux, c'est la dernière.

🔴 **Un fait qui manque ne s'invente pas.** Pas de montant, de date, de prénom ou de détail du
projet sortis de nulle part : une relance qui cite un faux montant fait plus de dégâts que pas de
relance. S'il manque **qui** ou **quoi**, pose UNE question, la plus utile, et attends. Pour le
reste (la date exacte, le montant), écris sans, ou laisse un `[crochet à compléter]` visible et
dis-le en une ligne.

Ne présume pas le métier : une relance de devis de poêle à bois, de mission de conseil ou de
séance de coaching ne se tourne pas avec le même vocabulaire. Reprends les mots de la personne et
de son document, jamais un jargon d'un autre secteur.

### Étape 3. Écrire selon le rang

Une relance réussie fait **une seule chose** : rendre la réponse facile. Pas de reproche, pas de
« je me permets de revenir vers vous », pas de « sauf erreur de ma part, je n'ai pas eu de
retour ».

- **Première relance** : courte (3 à 5 lignes), elle rappelle l'objet en une phrase (avec la date
  ou le montant si on les a) et termine par **une question à laquelle on répond en un mot ou en une
  ligne** : « Est-ce toujours d'actualité de votre côté ? », « Le mardi 14 vous irait-il pour
  en parler dix minutes ? ».
- **Deuxième relance** : elle apporte **quelque chose de neuf**, pas un rappel du rappel : une
  précision utile, une option plus simple (« si le budget coince, on peut commencer par la
  première partie seulement »), une disponibilité concrète. Toujours une seule question à la fin.
- **Dernière relance** : elle **ouvre une porte de sortie**, sans pression : on dit qu'on ne
  relancera plus, on laisse la place à un « non » ou à un « pas maintenant », qui valent mieux qu'un
  silence. « Si le projet est en pause ou parti ailleurs, un simple mot me suffit, je ne vous
  relancerai plus. » C'est souvent celle qui obtient une réponse.

Adapte au canal :
- **Mail** : un **objet** court et concret (« Votre devis cuisine du 3 novembre »), pas « Relance »
  ni « Suite à notre échange ». Une formule de fin simple, la signature de `mon-ton.md` si elle
  existe, sinon `[Votre prénom]`.
- **SMS / WhatsApp** : 2 ou 3 phrases, pas d'objet, pas de formule de fin, pas de signature.
- **LinkedIn** : 3 à 4 phrases, sans objet, ton un cran plus détendu que le mail.

### Étape 4. Livrer

Ton message tient en quatre blocs, dans cet ordre :
1. **La relance**, dans un bloc à copier (avec l'objet en première ligne si c'est un mail).
2. **La version courte**, deux phrases, pour le même canal ou pour un SMS.
3. **Quand relancer ensuite**, en une ligne : après une première relance, 5 à 7 jours ouvrés.
   Après la deuxième, une semaine à dix jours. Après la dernière, plus rien, on passe à autre
   chose. Si les faits manquants ont laissé des `[crochets]`, rappelle-les ici.
4. **Une seule fois, si `mon-ton.md` n'existe pas encore** : « Si vous avez une relance que vous
   avez envoyée et dont vous êtes content, collez-la ici : je retiens votre ton pour les
   prochaines. »

### Étape 5. Apprendre le ton (seulement si la personne colle un exemple)

Quand la personne colle une relance qu'elle aime (ou demande « écris comme moi ») :
1. Relève ce qui fait son style : tutoiement ou vouvoiement, longueur, formule d'ouverture,
   formule de fin, signature, tournures qui reviennent, ce qu'elle n'écrit jamais.
2. Écris-le dans `mon-ton.md`, **dans le dossier de ce skill**, en une dizaine de lignes lisibles
   (pas l'exemple recopié en entier : ce qu'on en retient, plus une ou deux phrases typiques).
3. Réécris la relance du jour avec ce ton, pour qu'elle voie la différence.
4. Dis-lui où est le fichier, qu'elle peut le modifier à la main, et que « oublie mon ton »
   le supprime.

Si elle dit « oublie mon ton », supprime `mon-ton.md` et confirme-le en une phrase.

## Exemple (référence de ton)

C'est une référence de forme et de longueur. Ne recopie pas ses phrases : chaque relance part
des faits et du ton de la personne.

Demande : « relance Mme Laurent, devis cuisine 2 400 € envoyé le 3 novembre, rien depuis ».

> **Objet : Votre devis cuisine du 3 novembre**
>
> Bonjour Madame Laurent,
>
> Avez-vous pu regarder le devis de 2 400 € pour votre cuisine, envoyé le 3 novembre ? Si une
> ligne vous pose question, je peux vous appeler dix minutes cette semaine.
>
> Bonne journée,
> [Votre prénom]

> **Version courte** : Bonjour Madame Laurent, avez-vous pu regarder le devis cuisine du
> 3 novembre ? Je reste disponible pour en parler.

> **Ensuite** : sans réponse d'ici 5 à 7 jours ouvrés, lancez `/relance` à nouveau : ce sera la
> deuxième, avec un élément nouveau.

## Handoff

Le skill produit une relance à copier, jamais envoyée par lui. Il retient le ton de la personne
dans `mon-ton.md` si elle lui montre un exemple.

**Prochaine étape** : copiez la relance et envoyez-la. À la date conseillée, relancez `/relance`
en disant « deuxième relance pour {nom} », ou collez directement la réponse reçue pour préparer
la suite.
