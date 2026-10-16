# Culturama — Analyse du projet

*Analyse réalisée le 16 octobre 2026*

## 1. Le concept en une phrase

Chaque jour, l'application tire un sujet au hasard (santé, histoire, IA…), propose un texte court et précis sur ce sujet. L'utilisateur résume ensuite **à voix haute** ce qu'il a compris, reçoit une note et des lectures pour aller plus loin.

## 2. Avis objectif : est-ce intéressant ?

**Oui, mais pas pour les raisons qu'on croit.** Lire des textes de culture générale, beaucoup d'applications le proposent déjà. Ce qui est rare et précieux, c'est **le résumé oral évalué par l'IA**.

### Points forts
| Point fort | Pourquoi c'est important |
|---|---|
| **Rappel actif par la voix** | Reformuler avec ses mots (« effet de génération », technique de Feynman) fait bien mieux retenir que relire ou cocher un QCM. C'est une différence pédagogique réelle. |
| **Expression orale** | La boucle travaille aussi l'aisance à l'oral, utile pour les entretiens, les concours et les présentations. On peut vendre ça au-delà de la « culture G ». |
| **Faisabilité en 2026** | La transcription vocale (Whisper, Deepgram, APIs natives iOS/Android) et l'évaluation par LLM sont devenues fiables et peu coûteuses. Un MVP se fait en quelques semaines. |
| **Marché francophone peu servi** | Les acteurs du micro-learning sont surtout anglophones. En français, l'offre se limite à des quiz (« Qui veut gagner des millions ») ou à des faits du jour, comme *Ça m'intéresse*. |
| **Boucle de rétention naturelle** | Une session courte par jour (environ 5 min), une note et une série de jours consécutifs : c'est le format qui fidélise (Duolingo, Wordle). |

### Points faibles et risques
| Risque | Gravité | Commentaire |
|---|---|---|
| **Friction du micro** | 🔴 Élevée | Parler à son téléphone dans les transports ou au bureau gêne. Beaucoup ne le feront pas. **Il faut proposer une alternative écrite** sinon la fonction phare sera boudée. |
| **Hasard pur = frustration** | 🟠 Moyenne | Tomber 3 fois de suite sur un sujet qui ne vous intéresse pas, c'est la désinstallation. Le hasard doit être *guidé*. |
| **Fiabilité des textes générés par IA** | 🔴 Élevée | Les hallucinations (fausses dates, faux chiffres, en santé surtout) détruisent la crédibilité. Il faut une vérification des faits et des sources citées. |
| **Recommandations d'ouvrages inventées** | 🟠 Moyenne | Les LLM inventent des livres qui n'existent pas. Il faut s'appuyer sur une vraie base (Google Books, Open Library, Babelio, ISBN). |
| **Note perçue comme arbitraire** | 🟠 Moyenne | Un « 12/20 » sans explication frustre. La note doit être détaillée et justifiée. |
| **Coût par session** | 🟢 Faible | Transcription et évaluation coûtent quelques centimes par session. C'est gérable, mais à surveiller pour une offre gratuite. |
| **Concurrence qui copie** | 🟠 Moyenne | Une fonction « résumé vocal » peut être ajoutée par un concurrent bien financé. L'avantage durable viendra du contenu, de la communauté et de la langue. |

**Verdict : 7/10 en l'état, potentiellement 8,5/10** avec les ajustements de la section 5. L'idée est bonne parce qu'elle mise sur la *compréhension* plutôt que la *consommation*. Le danger serait d'en faire « une appli de lecture de plus ».

## 3. Étude de marché

### Taille et tendance
- Le marché mondial du **micro-learning** est estimé autour de **2,6 à 3,2 milliards $ en 2025**. Selon les cabinets, la croissance annuelle va de **11 à 15 %**. Par exemple, Mordor Intelligence prévoit 2,96 Md$ en 2025 et 5,49 Md$ en 2030 (TCAC de 13 %). Ces chiffres viennent de rapports payants : ils donnent une tendance, pas une mesure précise.
- Les tendances de fond vont dans le sens du projet : formats courts sur mobile, lassitude face aux réseaux sociaux (« je veux scroller utile ») et adoption massive des assistants IA.

### Cibles potentielles
1. **Curieux de 25 à 45 ans** qui veulent « se cultiver » au lieu de scroller. C'est la cible principale des applis du type Headway ou Imprint.
2. **Étudiants et candidats aux concours** (Sciences Po, fonction publique, écoles de commerce, entretiens) : la culture générale *et* l'oral sont évalués. C'est une cible très motivée qui accepte de payer.
3. **Seniors** qui veulent stimuler leur mémoire. Le côté « entraînement cérébral » parle à cette cible.
4. **Entreprises (B2B)**, pour la formation continue et l'aisance à l'oral des équipes.
5. **Afrique francophone** : population jeune, très mobile, avec une forte demande de préparation aux concours. C'est peu adressé par les acteurs occidentaux.

### Concurrents

#### Concurrents directs (texte court + culture générale)
| Application | Ce qu'elle fait | Différence avec Culturama |
|---|---|---|
| **Curio AI : Daily Knowledge** | Leçons courtes (sciences, histoire, psychologie), quiz quotidiens, multilingue | Évaluation par quiz, pas de résumé oral |
| **Nerdish** | Articles de 5 à 10 min vérifiés, culture générale | Lecture passive, anglophone |
| **GenK, MyGrowth, BeClever** | Micro-leçons, audio, quiz, séries de jours | Quiz classiques |
| **Sapiens Club** | Articles courts histoire et sciences, « trivia battles » | Aspect compétitif, pas d'oral |
| **Ça m'intéresse (appli)** | Fait du jour en français par notification, podcasts | Très court, pas d'évaluation |
| **Coach Culturel, Culture générale pour concours** | QCM en français par catégorie, préparation aux concours | Quiz uniquement, peu de contenu à lire |

#### Concurrents indirects (formats proches)
| Application | Positionnement |
|---|---|
| **Blinkist, Headway, Imprint** | Résumés de livres et cours visuels, abonnement d'environ 60 à 90 €/an. Ce sont les leaders du « se cultiver en 15 min ». |
| **Elevate, Brilliant** | Entraînement cérébral et apprentissage interactif (maths, logique) |
| **Duolingo** | Pas le même sujet, mais c'est la référence pour la ludification et la rétention |
| **ChatGPT, Claude, Gemini (mode vocal)** | Un utilisateur motivé peut déjà demander « explique-moi un sujet puis évalue mon résumé ». C'est le vrai concurrent invisible : **la valeur doit venir de l'expérience guidée, du contenu sélectionné et de la régularité**, pas seulement de l'IA. |

#### Applications « explique à voix haute » (la fonction phare)
| Application | Ce qu'elle fait |
|---|---|
| **Feynman AI : Explain to Learn** | On explique un concept à l'oral ou à l'écrit et on reçoit un score de clarté et les points faibles |
| **Einstein AI** | Approche centrée sur la voix : on parle du sujet, on répond aux quiz à l'oral, avec une analyse par sous-thème |
| **ReExplain** (Product Hunt) | Partenaire de rétroaction pour apprendre en réexpliquant |

➡️ **Constat clé** : la mécanique « explique à voix haute et sois évalué » existe déjà, mais dans des **outils d'étude** où l'utilisateur apporte son propre sujet. Les applis de **culture générale quotidienne**, elles, se limitent aux quiz. **Personne ne combine bien les deux, surtout en français.** C'est la place à prendre.

## 4. Positionnement recommandé

> **« Le Duolingo de la culture générale, où l'on apprend en expliquant. »**
> 5 minutes par jour : je lis, je reformule, je progresse, et je deviens capable d'en parler.

La promesse n'est pas « savoir plus de choses », c'est **« être capable d'en parler »**, en dîner, en entretien ou en concours. C'est concret, ça se mesure et ça justifie l'oral.

## 5. Suggestions pour améliorer le produit

### 5.1 Corriger les faiblesses du concept initial
1. **Hasard guidé plutôt que hasard pur** : à l'inscription, l'utilisateur choisit ses thèmes préférés. Le tirage mélange ensuite environ 70 % de thèmes aimés et 30 % de découverte. On peut proposer de **relancer le dé** une fois par jour, et afficher 3 sujets tirés au sort pour en choisir un.
2. **Oral OU écrit** : le micro reste la fonction phare, mais un mode écrit est indispensable (transports, bureau, accessibilité pour les personnes malentendantes ou bègues).
3. **Une note expliquée** : au lieu d'un « 14/20 » sec, on détaille sur 4 critères :
   - ✅ Idées clés retrouvées (3 sur 4)
   - ❌ Erreurs ou contresens
   - 🗣️ Clarté et structure
   - 💡 Le point oublié le plus important, avec le passage du texte surligné
4. **Fiabilité du contenu** :
   - textes générés **puis relus**, ou appuyés sur des sources (Wikipédia, articles scientifiques) par une approche RAG ;
   - **sources affichées** en bas de chaque texte ;
   - un bouton « signaler une erreur » ;
   - une prudence renforcée sur la santé (avertissement, pas de conseil médical).
5. **De vrais livres** : recommandations reliées à une base réelle (Open Library, Google Books, ISBN), avec la couverture, un lien vers une librairie (affiliation Fnac, Amazon, Librairies indépendantes) et éventuellement des podcasts, documentaires ou vidéos en plus.

### 5.2 Fonctions qui renforcent la rétention
6. **Répétition espacée** : revenir sur un sujet lu il y a 3 jours, puis 2 semaines, avec une question rapide (« Te souviens-tu de… ? »). C'est ce qui transforme la lecture en savoir durable.
7. **Séries de jours, niveaux, badges**, de façon discrète, à la Duolingo.
8. **Carte de connaissances** : visualiser ses thèmes maîtrisés (« 12 sujets en histoire, 3 en IA ») et ses lacunes.
9. **Questions de relance par l'IA** : après le résumé, l'IA pose 1 ou 2 questions de compréhension (« Pourquoi selon toi… ? »). On passe du résumé à une vraie discussion.
10. **Plusieurs niveaux de difficulté** pour le même sujet (découverte, intermédiaire, expert).
11. **Version audio du texte**, pour écouter en marchant puis résumer.

### 5.3 Fonctions sociales et virales
12. **Défi entre amis** : même sujet du jour pour tout le monde, comparaison des notes (l'effet Wordle).
13. **Carte partageable** : « J'ai appris aujourd'hui pourquoi… », à poster sur Instagram, LinkedIn ou WhatsApp.
14. **Classements** par ville, par école ou par entreprise.

### 5.4 Déclinaisons à fort potentiel
15. **Mode concours / entretien** : sujets d'actualité et de culture G de type Sciences Po ou fonction publique, avec une évaluation orale façon jury. C'est probablement **le segment le plus rentable** au départ.
16. **Mode entreprise (B2B)** : parcours sur mesure (culture du secteur, conformité, aisance à l'oral).
17. **Mode famille / enfants** : textes adaptés par âge, résumé oral pour travailler l'expression.
18. **Multilingue** : résumer en anglais un texte lu en anglais, pour apprendre à la fois la culture générale et la langue.

## 6. Modèle économique suggéré

| Offre | Contenu | Prix indicatif |
|---|---|---|
| **Gratuit** | 1 sujet par jour, résumé écrit, note simple | 0 € |
| **Premium** | Sujets illimités, résumé oral, retour détaillé, répétition espacée, choix des thèmes, audio | 5 à 8 €/mois ou 40 à 60 €/an |
| **Concours** | Parcours de préparation, simulations d'oral | 10 à 15 €/mois, ou en pack |
| **B2B** | Licences entreprise ou école, tableau de bord | Par utilisateur |
| **Revenus annexes** | Affiliation sur les livres recommandés | Commission |

À surveiller : le **coût IA par session** (transcription + LLM), qui représente quelques centimes. Il faut limiter l'oral sur l'offre gratuite et mettre en cache les textes (un même texte est servi à plusieurs utilisateurs).

## 7. Feuille de route MVP proposée

| Phase | Durée | Contenu |
|---|---|---|
| **0. Validation** | 2 semaines | Page d'accueil et liste d'attente, 10 à 20 entretiens utilisateurs, test du résumé oral sur un prototype simple (même un Typeform avec audio) |
| **1. MVP** | 6 à 8 semaines | Application mobile (React Native/Expo ou Flutter), 6 à 8 thèmes, environ 100 textes relus, résumé oral et écrit, note détaillée, 3 livres réels par sujet, série de jours |
| **2. Rétention** | +1 à 2 mois | Répétition espacée, questions de relance, audio, notifications, partage |
| **3. Monétisation** | +1 mois | Premium, mode concours |
| **4. Croissance** | ensuite | Défis entre amis, B2B, autres langues |

**Indicateurs à suivre** : rétention à J1, J7 et J30 ; part des utilisateurs qui *font* le résumé après lecture (KPI n°1 : il valide ou invalide l'idée centrale) ; part oral/écrit ; conversion vers Premium.

### Pile technique indicative
- **Front** : React Native (Expo) ou Flutter
- **Transcription** : Whisper, Deepgram ou la reconnaissance vocale native iOS/Android
- **Génération et évaluation** : API d'un LLM (Claude, etc.) avec une grille d'évaluation structurée en JSON
- **Livres** : API Open Library / Google Books
- **Back** : Supabase ou Firebase (auth, base de données, stockage)

## 8. Conclusion

Culturama a une **vraie idée différenciante** : apprendre en reformulant à l'oral, appliqué à la culture générale du quotidien et **en français**. C'est un créneau encore peu occupé. Les principaux risques sont la gêne liée au micro, le hasard trop rigide et la fiabilité des contenus. Tous trois se corrigent facilement dès la conception.

**Prochaine étape recommandée** : valider l'hypothèse centrale, à savoir que les gens acceptent de résumer à voix haute, avec un prototype minimal avant de développer l'application complète.

---

### Sources
- [Curio AI : Daily Knowledge (App Store)](https://apps.apple.com/app/id6739725206)
- [Nerdish : Daily Smart Learning](https://mwm.ai/>/apps/nerdish-daily-smart-learning/1552613187)
- [Sapiens Club (App Store)](https://apps.apple.com/app/id6754659539)
- [GenK : World General Knowledge (App Store)](https://apps.apple.com/app/id6612027371)
- [MyGrowth : Daily Micro Learning](https://apps.appfollow.io/ios/mygrowth-daily-micro-learning/6748383002?country=ca)
- [BeClever : Learning Every Day](https://appgoblin.info/apps/6741388378)
- [digiSchool : Top 10 des applis pour booster sa culture générale](https://www.digischool.fr/articles/culture-generale/top-10-des-applis-pour-booster-sa-culture-generale/)
- [Culture générale pour concours (App Store)](https://apps.apple.com/us/app/id1485934291)
- [Quiz Culture Générale Français (App Store)](https://apps.apple.com/FR/app/id854406658)
- [Feynman AI : Explain to Learn (App Store)](https://apps.apple.com/in/app/feynman-ai-explain-to-learn/id6738237030?l=hi)
- [Einstein AI : Learn & Memorize (App Store)](https://apps.apple.com/us/app/einstein-ai-learn-memorize/id6739162816?l=ar)
- [ReExplain (Product Hunt)](https://www.producthunt.com/posts/reexplain)
- [MemX : la technique de Feynman avec un partenaire d'étude IA](https://memx.app/blog/feynman-technique-ai-study-partner/)
- [Research and Markets : marché du micro-learning (Mordor Intelligence)](https://www.researchandmarkets.com/reports/5120128/microlearning-market-share-analysis-industry)
- [Technavio : marché du micro-learning](https://technavio.com/report/microlearning-market-industry-analysis)
- [TechSci Research : marché du micro-learning](https://giiresearch.com/report/tsci1586598-microlearning-market-global-industry-size-share.html)
- [UBC ETEC522 : micro-learning (chiffres IMARC)](https://blogs.ubc.ca/etec522/?p=7589)

*Les informations sur Blinkist, Headway, Imprint, Elevate, Brilliant et Duolingo viennent de connaissances générales, pas d'une recherche récente. Leurs prix et fonctions actuels sont à vérifier.*
