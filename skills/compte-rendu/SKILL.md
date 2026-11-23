---
name: compte-rendu
description: "Utilise CE skill DÈS QUE l'utilisateur veut tirer quelque chose d'une réunion ou d'un appel : il dit « compte-rendu », « fais-moi le CR », « résume la réunion », « qui doit faire quoi ? », colle un transcript, des notes en vrac ou donne un fichier d'enregistrement transcrit (.txt, .vtt, .srt, .md, .pdf), même sans demande explicite. Produit un compte-rendu structuré : l'essentiel en une phrase, les décisions, les actions (qui, quoi, pour quand), les questions restées ouvertes. N'invente jamais un responsable ni une échéance. Apprend la structure de l'utilisateur à partir d'un CR qu'il aime."
allowed-tools: Read, Write, Edit, Glob
---

# /compte-rendu : un transcript en vrac devient un CR qu'on peut envoyer

## Pour quoi faire

**Entrée** : ce qui reste d'une réunion. Un transcript collé (Zoom, Meet, Teams, un enregistreur,
une appli de dictée), un fichier transcrit dans le dossier, ou des notes prises à la main, en
désordre.
**Sortie** : **un compte-rendu en fichier**, prêt à relire et à envoyer : ce qui a été décidé, qui
fait quoi et pour quand, ce qui reste ouvert. Et son résumé à l'écran.

L'effet magique : une heure de réunion, quarante pages de transcript, et en une minute on sait
qui doit faire quoi. Rien n'a été inventé pour combler les trous.

## Aucune dépendance

Ce skill ne dépend d'aucun outil externe, il marche immédiatement. Il ne transcrit pas l'audio :
il part d'un texte. Si la personne n'a qu'un enregistrement, dis-lui que la plupart des outils de
visio (Zoom, Meet, Teams) et beaucoup d'enregistreurs produisent un transcript, et qu'il suffit de
le coller.

## Comment procéder

> *(Instructions pour toi, le skill. « Tu » = toi qui exécutes. « Vous » = la personne qui t'a
> lancé.)*

### Étape 1. Lire la mémoire du skill

Regarde si `mon-modele-cr.md` existe **dans le dossier de ce skill** (le dossier qui contient ce
`SKILL.md`). S'il existe, c'est la structure que la personne veut : ses sections, leur ordre, son
niveau de détail, son ton. Tu la suis à la lettre à la place du modèle par défaut de l'étape 3.

### Étape 2. Trouver la matière

- Un transcript ou des notes **collés** : c'est la matière.
- Un **fichier** cité : lis-le. `.txt`, `.md`, `.vtt`, `.srt` et `.pdf` se lisent directement. Un
  `.docx` ne se lit pas tel quel : demande à la personne de l'enregistrer en PDF ou en texte, ou
  d'en coller le contenu.
- **Rien du tout** (`/compte-rendu` seul) : regarde si le dossier courant contient un transcript
  récent (`*.vtt`, `*.srt`, `*transcript*`, `*reunion*`, `*notes*`). S'il y en a un, propose-le et
  attends la confirmation. Sinon, demande de coller le texte.

Avant d'écrire, repère dans le texte : la date (sinon, demande-la ou écris `[date]`), le sujet,
les participants. Si le transcript ne nomme pas les gens (« Intervenant 1 », « Speaker 2 »), garde
ces étiquettes, n'invente pas de noms, et propose à la fin : « dites-moi qui est qui, je remplace ».

### Étape 3. Écrire le CR (modèle par défaut)

Le fichier suit cet ordre, chaque section n'apparaît que si elle a du contenu :

1. **En-tête** : sujet, date, participants (et les absents s'ils sont cités).
2. **En une phrase** : ce qu'il faut retenir si on ne lit que ça.
3. **Décisions** : ce qui a été **tranché**, une puce par décision, formulée comme un fait
   (« Le lancement est repoussé au 15 janvier »). Une piste évoquée n'est pas une décision : elle va
   dans les questions ouvertes.
4. **Actions** : un tableau **Qui · Quoi · Pour quand**. Une ligne par action, le verbe d'action
   en tête (« Envoyer le devis révisé »).
5. **Questions ouvertes** : ce qui reste à trancher, et qui doit le faire si c'est dit.
6. **Ce qui s'est dit** : par sujet abordé, trois à cinq lignes chacun, pour celui qui n'était pas
   là. Pas un résumé chronologique de chaque prise de parole.

🔴 **Les règles qui font la confiance dans un CR** :
- **Pas de responsable ni d'échéance inventés.** Si personne n'a dit qui s'en charge, la case dit
  `à définir`. Si aucune date n'a été dite, `non fixée`. Un CR qui attribue une tâche à quelqu'un
  qui ne l'a jamais acceptée crée un conflit à la réunion suivante.
- **Pas de décision fabriquée.** En cas de doute (« on pourrait peut-être… »), c'est une question
  ouverte.
- **Les chiffres, dates et noms propres sont recopiés** tels qu'ils apparaissent. Si le transcript
  est visiblement faux sur un mot (un nom écorché par la transcription), garde-le et signale-le
  dans ton message, ne le corrige pas au hasard.
- **Les mots de la réunion, pas un jargon plaqué.** Ne présume pas le métier des participants.

Écris le fichier dans le dossier courant : `compte-rendu-AAAA-MM-JJ-<sujet-court>.md` (la date de
la réunion, le sujet en deux ou trois mots). S'il existe déjà, ajoute `-2`.

### Étape 4. Livrer

Ton message tient en peu de lignes :
1. le chemin du fichier ;
2. la phrase « En une phrase » ;
3. le tableau des actions (c'est ce qu'on regarde en premier) ;
4. ce que tu as laissé à `à définir`, `non fixée` ou `[à compléter]`, et les mots douteux, pour
   qu'elle sache quoi vérifier avant d'envoyer ;
5. **une seule fois, si `mon-modele-cr.md` n'existe pas encore** : « Si vous avez un compte-rendu
   dont vous êtes content, collez-le ou donnez-moi son fichier : je retiens votre structure pour
   les prochains. »

### Étape 5. Apprendre la structure (seulement si la personne donne un exemple)

Quand la personne fournit un CR qu'elle aime :
1. Relève sa structure : les sections et leur ordre, leurs titres exacts, la forme des actions
   (tableau, liste, initiales), la longueur, le ton, ce qui est en gras.
2. Écris-la dans `mon-modele-cr.md`, **dans le dossier de ce skill** : la liste des sections avec
   une ligne sur ce que chacune contient. Pas le CR recopié : sa forme. Rien de son contenu
   (noms, chiffres, sujets) ne doit s'y retrouver.
3. Refais le CR du jour dans cette structure.
4. Dis-lui où est le fichier, qu'elle peut le modifier à la main, et que « oublie mon modèle »
   le supprime.

Si elle dit « oublie mon modèle », supprime `mon-modele-cr.md` et confirme-le en une phrase.

## Exemple de tableau d'actions (référence)

| Qui | Quoi | Pour quand |
|---|---|---|
| Sophie | Envoyer le devis révisé avec l'option pose | vendredi 21 |
| Karim | Vérifier les disponibilités de l'équipe en janvier | non fixée |
| à définir | Prévenir le fournisseur du changement de date | avant le 15 janvier |

## Handoff

Le skill produit un fichier `compte-rendu-….md` dans le dossier courant et son résumé à l'écran.
Il retient la structure préférée de la personne dans `mon-modele-cr.md` si elle lui montre un
exemple.

**Prochaine étape** : relisez les cases `à définir`, puis demandez « fais-en un mail pour les
participants » pour l'envoyer, ou relancez `/compte-rendu` sur la réunion suivante.
