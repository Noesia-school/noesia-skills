---
name: prep-rdv
description: "Utilise CE skill DÈS QUE l'utilisateur a un rendez-vous, un appel ou une visio à préparer : il dit « prépare mon rendez-vous », « prep rdv », « j'ai un appel avec… demain », « qui est cette personne ? », « je vois tel client tout à l'heure », ou donne un nom, une société, un site ou un profil avant une rencontre, même sans demande explicite. Cherche sur le web qui est la personne et ce que fait sa structure, puis écrit une fiche d'une page : qui c'est, l'objectif du rendez-vous, les questions à poser, les objections probables. Chaque fait trouvé porte sa source, rien n'est inventé."
allowed-tools: WebSearch, WebFetch, Read, Write, Edit, Glob
---

# /prep-rdv : un nom avant un rendez-vous, une fiche d'une page qui vous prépare

## Pour quoi faire

**Entrée** : la personne ou la structure qu'on va voir (un nom, une société, un site, un profil
copié), et si possible pourquoi on la voit (« premier appel, elle cherche quelqu'un pour refaire
son site », « rendez-vous banque pour le prêt »).
**Sortie** : **une fiche d'une page**, en fichier : qui elle est, ce que fait sa structure, ce que
vous voulez obtenir de ce rendez-vous, les questions à poser, les objections à prévoir. Chaque
information trouvée sur le web porte son lien.

L'effet magique : dix minutes avant l'appel, au lieu d'ouvrir quinze onglets, vous lisez une
page et vous arrivez en sachant à qui vous parlez.

## Aucune dépendance à installer

Ce skill ne dépend d'aucun programme à installer. Il utilise la recherche web de Claude Code
(`WebSearch`, `WebFetch`). Si ta session n'a pas d'outil de recherche web, il travaille avec ce que
la personne lui donne (un site, un texte collé) et le dit.

## Comment procéder

> *(Instructions pour toi, le skill. « Tu » = toi qui exécutes. « Vous » = la personne qui t'a
> lancé.)*

### Étape 1. Lire la mémoire du skill

Regarde si `mon-activite.md` existe **dans le dossier de ce skill** (le dossier qui contient ce
`SKILL.md`). S'il existe, c'est ce que fait la personne qui t'a lancé (son métier, ce qu'elle
vend, à qui) : il sert à écrire l'objectif, les questions et les objections. S'il n'existe pas,
regarde le `CLAUDE.md` du projet et la conversation. Si rien ne le dit, n'invente pas son métier :
écris des questions et des objections valables pour tout premier rendez-vous, et propose à la fin
de retenir son activité (étape 5).

### Étape 2. Cerner le rendez-vous

Il te faut **qui** (un nom, une société, un site) et, si possible, **pourquoi** (le type de
rendez-vous et ce qu'on en attend). Ne redemande pas ce qui est déjà dit. Si le « qui » manque,
pose UNE question. Si le « pourquoi » manque, ne bloque pas : fais la fiche, et l'objectif dira
`[à préciser]`.

### Étape 3. Chercher, et s'assurer que c'est la bonne personne

1. Fais 2 à 4 recherches web : la personne avec sa structure, la structure seule (site officiel,
   activité, taille, actualité récente), et ce que la personne a publié ou dit en public si ça
   existe. Ouvre le site officiel de la structure s'il y en a un.
2. **Homonymes** : si le nom correspond à plusieurs personnes et que rien ne permet de trancher
   (ni la structure, ni la ville, ni le métier), arrête-toi et demande laquelle, en listant les
   deux ou trois candidates en une ligne chacune. Une fiche sur la mauvaise personne est pire que
   pas de fiche.
3. **LinkedIn ne s'ouvre pas aux robots** : une page de profil renvoie une page de connexion.
   N'essaie pas de la deviner. Si la personne veut le profil dans la fiche, elle copie le texte de
   la page et le colle : tu le lis comme une source.
4. Si la personne a donné des fichiers ou des notes (anciens échanges, mail de prise de contact),
   lis-les : c'est souvent la meilleure source.

🔴 **Chaque fait vient d'une source que tu as lue.** À côté de chaque information trouvée sur le
web, son lien. Ce que tu n'as pas trouvé, tu l'écris « non trouvé », tu ne le complètes pas avec
une supposition (taille de l'entreprise, chiffre d'affaires, poste, âge). Les hypothèses ont leur
place dans les questions à poser, formulées comme des questions.

### Étape 4. Écrire la fiche (une page, pas plus)

Fichier dans le dossier courant : `prep-rdv-<nom-court>-AAAA-MM-JJ.md` (la date du rendez-vous si
elle est connue, sinon celle du jour). Les sections, dans cet ordre :

1. **En une phrase** : qui vous voyez et pourquoi ça compte.
2. **Qui c'est** : la personne (rôle, parcours utile au rendez-vous), 3 à 5 lignes sourcées.
3. **Sa structure** : ce qu'elle fait, pour qui, sa taille si elle est publique, une actualité
   récente si elle existe. 3 à 5 lignes sourcées.
4. **Ce que vous voulez obtenir** : l'objectif du rendez-vous en une phrase, et la suite idéale
   (« un deuxième rendez-vous avec l'associé », « l'accord pour envoyer un devis »).
5. **Questions à poser** : 5 questions ouvertes, dans l'ordre où elles viennent dans la
   conversation, chacune utile pour atteindre l'objectif.
6. **Objections probables** : 2 ou 3, chacune avec une piste de réponse en une ligne.
7. **Pour ouvrir** : une phrase d'accroche qui montre qu'on s'est renseigné (en s'appuyant sur un
   fait sourcé de la fiche), sans flatterie.
8. **Sources** : la liste des liens lus.

Ne présume pas le métier de la personne rencontrée ni le vôtre : un rendez-vous chez un artisan,
un banquier ou une directrice d'école ne se prépare pas avec le même vocabulaire.

### Étape 5. Livrer

Ton message : le chemin du fichier, la phrase « En une phrase », les 5 questions, et ce que tu n'as
pas trouvé (ou le doute sur l'identité, s'il en reste un). **Une seule fois, si `mon-activite.md`
n'existe pas encore** : si la personne a déjà dit ce qu'elle fait (dans sa demande ou plus tôt
dans la conversation), ne le lui redemande pas, propose de le retenir : « Vous m'avez dit que
vous êtes {ce qu'elle a dit}. Je le retiens pour les prochaines fiches ? ». Sinon : « Dites-moi
en une phrase ce que vous faites et pour qui : je le retiens, et les prochaines fiches viseront
vos objectifs à vous. » Quand elle répond ou accepte, écris sa phrase dans
`mon-activite.md` (dans le dossier de ce skill), dis-lui où est le fichier et que « oublie mon
activité » le supprime. Si elle le demande, supprime-le et confirme en une phrase.

## Exemple de bloc « Questions à poser » (référence de ton)

> 1. Qu'est-ce qui vous a fait chercher quelqu'un maintenant, plutôt qu'il y a six mois ?
> 2. Qui d'autre participe à la décision ?
> 3. Qu'avez-vous déjà essayé, et qu'est-ce qui n'a pas marché ?
> 4. Si on se revoit dans trois mois et que tout s'est bien passé, qu'est-ce qui a changé pour vous ?
> 5. Quelle est la prochaine étape de votre côté après notre échange ?

## Handoff

Le skill produit une fiche `prep-rdv-….md` d'une page dans le dossier courant, chaque fait avec
son lien. Il retient l'activité de la personne dans `mon-activite.md` si elle la lui donne.

**Prochaine étape** : relisez la fiche juste avant le rendez-vous. Après, collez vos notes ou le
transcript et lancez `/compte-rendu` si vous l'avez, ou `/relance` si la personne tarde à
répondre.
