# Axon — ton second cerveau, branché sur tes IA

Axon transforme un simple dossier de notes (sur ton PC ou dans Google Drive) en **mémoire persistante** que tes IA partagent. Claude, mais aussi Cursor, Codex ou Gemini peuvent y lire, chercher par le sens, écrire et relier tes notes, et modifier tes fichiers Excel, Word ou PowerPoint. Rien n'est jamais supprimé.

Toi, tu vois ton cerveau en 3D : chaque note est une étoile, chaque domaine de ta vie une nébuleuse de couleur.

> Ce dépôt contient **les installateurs** d'Axon pour Windows 10 et 11 (64 bits).

---

## Installer
1. Ouvre **[Releases](../../releases/latest)** et télécharge **`Axon-Setup-x.y.z.exe`**.
2. Double-clique dessus, puis suis l'assistant : dossier d'installation → **Installer** → **Terminer**.
   - Rien à taper, pas de terminal, pas de Node.js à installer : tout est dans l'installateur.
   - Si Windows affiche « Windows a protégé votre ordinateur » : *Informations complémentaires* → *Exécuter quand même*. L'installateur n'est pas encore signé par un certificat payant.
3. **Les mises à jour sont automatiques.** Quand une nouvelle version sort, un bandeau propose « Redémarrer pour mettre à jour ».

## Le premier lancement
Axon te pose 3 questions :
1. **Ton prénom.** Il signe ton journal et tes actions.
2. **Où vit ton cerveau.**
   - **Cloud** : un dossier dans Google Drive, OneDrive ou Dropbox. Il est synchronisé sur tes appareils et partageable.
   - **Personnel** : un dossier sur ce PC.
   Le dossier choisi devient la racine, et tout se crée dedans. Si tu choisis un dossier qui est déjà un cerveau Axon, tu le **rejoins**.
3. **Tes domaines de vie** : par exemple École, Business, Finance, Trading. Tu pourras en ajouter à tout moment.

Laisse cochée la case **« Brancher automatiquement Claude »**. Ensuite, quitte Claude Desktop complètement (clic droit sur son icône près de l'horloge → *Quitter*), rouvre-le, et écris : `Appelle brain_demarrer`.

---

## Ce qu'Axon sait faire

| | |
|---|---|
| **Cerveau 3D** | Des nuées de particules par domaine, et trois formes : cerveau, cerveau + colonne vertébrale, galaxie. « Voir grandir » rejoue la croissance de ton cerveau, et la vue épurée retire l'interface. La qualité s'adapte toute seule à ta carte graphique. |
| **Claude dans Axon** (bouton *Claude* ou `Ctrl+J`) | Le chat Claude Code, à côté du cerveau. Tu choisis le modèle (Opus, Sonnet ou Haiku) et les permissions, tu retrouves tes anciens chats et ta consommation, et tu peux parler au micro. Les notes que Claude crée apparaissent en direct dans la 3D. Il faut Claude Code installé et connecté. |
| **Jeff, le routeur** | Chaque demande va au bon niveau : des règles locales instantanées, sans IA ; un modèle rapide gratuit qui connaît tout ton cerveau ; ou Claude pour le vrai travail. Réglages : `Ctrl+K` → *Réglages IA*. |
| **Jarvis** (onglet *Jarvis* ou touche `V`) | Tu lui parles à voix haute (maintiens *Espace* ou dis « Hey Jarvis »). Il répond en voix française et t'emmène dans le cerveau : « emmène-moi à mes objectifs », « où en est le projet ? ». |
| **Voix 100 % locale** | Whisper pour écouter et Kokoro pour parler. L'audio ne quitte jamais ton PC. |
| **Fichiers Office** | Excel, Word et PowerPoint rangés dans leurs notes. Les IA les lisent et les modifient sur place, mise en forme gardée, et l'ancienne version est toujours conservée. |
| **Recherche par le sens** | « montre noire » trouve aussi « cadran sombre ». Le modèle tourne sur ton PC. |
| **Consignes** | Chaque remarque que tu fais à une IA est notée, rangée et respectée ensuite par toutes les IA. |

### Activer le modèle rapide (gratuit)
`Ctrl+K` → **Réglages IA**, puis colle une clé gratuite :
- **Gemini** : <https://aistudio.google.com/apikey>
- **Groq** : <https://console.groq.com/keys>
- **OpenRouter** : <https://openrouter.ai/keys>

Sans clé, Axon utilise un petit modèle local (Qwen), hors ligne mais plus limité. Les clés sont chiffrées sur ton PC et ne vont jamais dans le cerveau.

---

## Comment le cerveau est rangé
```
00-COMMENCER-ICI.md      l'accueil : qui tu es, tes domaines (la 1re page que lit une IA)
00-Inbox/                tout ce qui arrive en vrac · _archive/ = la « corbeille » récupérable
01-Journal/AAAA/         une note par jour et par personne
05-Noyau/                objectifs, mémoire des IA, consignes pour les IA
10- … 69-<Domaine>/      chaque domaine : un hub + Projets/ · Savoir/ · Decisions/ · Ressources/ · Archives/
70-Savoir/ 75-Personnes/ 80-Sources/      ce qui sert à plusieurs domaines
90-Fichiers/ 95-Flux/ 99-Systeme/         partie technique : index, carnet de bord, réglages
```
- **Un projet = un dossier = un neurone**, avec ses fichiers à côté.
- **Les liaisons :**
  - chaque note a un **parent** (son hub) ;
  - au moins deux **liens** vers d'autres endroits ;
  - les **hubs** servent de carte.
  L'IA lit le hub avant d'ouvrir 50 notes : elle ne se perd pas et consomme peu.
- Ce sont de simples fichiers Markdown, compatibles Obsidian : tu gardes tout, même sans Axon.

## Un cerveau à deux
1. Choisis **Cloud** et un dossier Google Drive.
2. Partage-le en *Éditeur* avec ton associé.
3. Lui ajoute un raccourci dans « Mon Drive », installe Axon et choisit **le même dossier** : il le rejoint.

Chacun a son journal et son carnet de bord : pas de conflit. La seule règle : ne modifiez pas la même note au même moment.

## Brancher d'autres IA
- **Claude Desktop et Claude Code** : branchés automatiquement. Sinon : `Ctrl+K` → *Brancher Claude*.
- **Cursor, Codex, Gemini CLI** : même serveur MCP. Voir le guide intégré (`Ctrl+K` → *Guide Axon*).
- **ChatGPT, Gemini web** : donne-leur le fichier `llms-full.txt` à la racine de ton cerveau. Il contient tout l'essentiel en un fichier et se met à jour tout seul.

---

## Vie privée et sécurité
- Tes notes restent dans **ton** dossier. La recherche par le sens et la voix tournent sur ton PC.
- **Ce qui sort de ton PC**, seulement si tu les utilises :
  - les questions envoyées au modèle rapide que tu as choisi (Gemini, Groq ou OpenRouter) ;
  - celles envoyées à Claude ;
  - les données publiques de l'accueil : marchés, crypto, météo.
- **Les IA n'effacent jamais rien** : « supprimer » veut dire archiver, et chaque modification garde l'ancienne version.
- Les chemins de fichiers sont confinés au cerveau, les dossiers cachés et les exécutables sont protégés, et le contenu des notes est traité comme une donnée, jamais comme un ordre.

## Désinstaller
**Paramètres Windows → Applications → Axon → Désinstaller.** Axon est aussi débranché de Claude. **Ton cerveau n'est jamais supprimé.**

## Questions fréquentes
- **« axon » n'apparaît pas dans Claude Desktop** : quitte Claude **complètement** (icône près de l'horloge → *Quitter*), puis rouvre-le.
- **Ça rame** : `Ctrl+K` → *Matériel utilisé* pour voir la carte graphique utilisée. La qualité du cerveau 3D se règle dans la roue crantée → *Qualité*.
- **Jarvis ne m'entend pas** : autorise le micro à Axon dans *Paramètres Windows → Confidentialité → Microphone*.
