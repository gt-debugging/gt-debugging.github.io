---
title: Sessions 2023
order: 1
---
Le GT Debugging aura deux sessions de présentations aux journées du GDR-GPL 2023 :
- Jeudi 8 juin de 14h à 15h30
- Jeudi 8 juin de 16h à 17h30
Le programme complet de la journée du GDR le 8 juin est visible ici https://gdrgpl2023.sciencesconf.org/program/graphic/date/2023-06-08

Les présentations du GT-Debugging seront donc réparties en deux sessions.

## Session 1 : 14h00 - 15h30

### 1 - Finding Faults of Executable Models: Manually and Automatically

**Faezeh Khorram** - HUAWEI technologies France.

**Abstract**

When a model represents the dynamic aspects of a system (a.k.a behavioral model), testing it becomes a necessitate to ensure it represents the correct behavior. If test cases fail, it alerts the existence of faults in the model, hereafter proper means are needed to localize the faults. In this presentation, I will talk about both manual and automatic fault localization techniques in the context of executable models and their test cases. In particular, the challenges of adopting the existing debugging techniques from the software testing area to the model testing area will be discussed. Finally, I will present a generic solution to tackle the challenges along with demonstrating the developed solution in an Eclipse environment.


### 2 - Protocol-Based Interactive Debugging for Domain-Specific Languages.

**Josselin ENET (speaker), Erwan BOUSSE, Massimo TISI, Gerson SUNYE** - Université de Nantes, équipe Naomod.

**Abstract**

Interactive debuggers are established tools used by developers to understand programs and localize faults.
They are equally valuable in the context of model-driven development, when working on executable behavioral models.
However, development costs of interactive debuggers for Domain-Specific Languages (DSLs) can be significant. In order to mitigate these costs, several reusable DSL-agnostic debugging solutions have been proposed.
We argue that the applicability of these solutions is limited by being tied to a fixed set of debugging services, a specific language engineering approach, or a particular user interface.
In this paper, we present a novel approach to provide interactive debugging services for executable DSLs through a reusable generic architecture.
We propose a protocol allowing a generic interactive debugger to communicate with heterogeneous DSL runtimes, both for controlling the execution and for configuring the debugger with domain-specific breakpoints.
The proposed debugger can itself be controlled using a reinterpretation of the Debug Adapter Protocol (DAP), for an effortless integration in existing Integrated Development Environments (IDEs) that support it.
Using a prototype implementation based on JSON-RPC and two heterogeneous DSL runtimes, we demonstrate that our approach provides an off-the-shelf reusable interactive debugger that supports meaningful domain-specific breakpoints, and that can be used with minimal effort within a standard IDE such as Visual Studio Code.


### 3 - Prototypage IHM pour la défense : déboguage et correctifs distribués à chaud et sans interruption de système collaboratifs en cours d’exécution.

**Pierre Laborde, Éric Le Pors** - Thales DMS, Brest.

**Abstract** 

Nous réalisons des prototypes d’interface homme-machine (IHM) pour différents domaines de la défense (Aérien, Terrestre, Maritime, etc.) dans le but de concevoir de futurs systèmes de mission. Pour mettre au point ces prototypes nous allons jusqu’à mettre en situation les utilisateurs avec des scénarios d’usages au travers d’évaluations ergonomiques. Les utilisateurs sont alors immergés dans une séance qui leur permet de réaliser les tâches de leur quotidien comme s'ils avaient le futur système entre leurs mains. Nos spécialistes UX (User Experience) et IHM observent alors les séances au travers des différents scénarios pour mieux récolter les retours utilisateurs, les problèmes, identifier les manques mais aussi mettre en avant et tester des nouvelles capacités ou ergonomies. Cependant, ces prototypes ne sont pas exempts de défauts : il y a parfois des bogues et des choses que nous n’avons pas anticipées. Ces séances sont longues, rares et difficiles à mettre au point, nous avons donc besoin de faire travailler au maximum les utilisateurs sans les interrompre et sans perturber le bon déroulé des scénarios. Il nous faut pouvoir résoudre tous les problèmes qui surviennent (dans la mesure du possible) pendant que le système est utilisé. Si le système doit être arrêté pour un problème, nous perdons parfois des heures de mise en situation et de contexte utilisateur. Nous avons mis au point des outils et des processus qui nous permettent d’intervenir directement pendant l’exécution, sans interruption majeure, et ceci alors que le système est utilisé de manière collaborative par plusieurs personnes en même temps. Nous expliquons dans cette présentation notre démarche au travers d’un exemple récent d’évaluation ergonomique sur prototype de système de surveillance maritime à bord d’un avion simulé avec un équipage de 5 personnes.

## Session 2 : 16h00 - 17h30

### 4 - Détection des anomalies d'ordonnancement dans un système temps réel.

**Blandine Djika (speaker), Georges Kouamou, Frank Singhoff, Alain Plantec** - Université de Bretagne Occidentale.

**Abstract**

Nos travaux portent sur les anomalies d'ordonnancement dans les systèmes temps réel. Dans un système temps réel, les tâches doivent être exécutées de sorte qu'elles respectent des contraintes temporelles telles que des échéances. Pour ce faire, les acteurs du domaine valident le comportement temporel des tâches lors des phases amonts de la conception du système. Toutefois, sous certaines conditions, il peut arriver que les échéances des tâches ne soient finalement pas respectées à l'exécution. C'est notamment le cas lors d'évènements contre intuitifs comme l'augmentation des ressources du système. On parle alors d'anomalies d'ordonnancement. Dans cet exposé, nous décrivons un modèle d'analyse permettant  la détection de ces anomalies d'ordonnancement. Nous montrons également comment exploiter ce modèle pour le développement d'un outil de monitoring sur POSIX/RTEMS appelé MONANO. MONANO permet de détecter ce type d'anomalies à l'exécution.

### 5 - Comment faciliter le processus de debugging en tracant la compilation.

**Bruno MATEU** - IMT Atlantique, Brest.

**Abstract**

Un processus de compilation moderne comporte plusieurs centaines de passes qui
peuvent chacune contenir plusieurs transformations. Ces transformations sont
appliquées sur le code de manière sélective, selon les options de configurations
données et des propriétés du code en entrée. À un code source et une
configuration donnée (contenant éventuellement une graine pour le générateur de
nombres aléatoires), le processus de compilation exécuté sera toujours le même.
Cependant, une modification — même légère — de la configuration ou du code peut
modifier la liste des transformations appliquées sur le code. Les
propriétés du code produit dépendent essentiellement des passes appliquées.

Pour cette raison retracer l'histoire d'une instruction telle qu'elle apparaît
dans le binaire, c'est-à-dire à quelle(s) ligne(s) de code source elle
correspond et quelles sont les transformations subies par celle(s)-ci, est
difficile. S'il est possible de connaître la liste des passes appelées lors d'un
processus de compilation, on ne peut pas savoir quelles sont les transformations
qu'une passe a réalisé sans comparer la représentation interne en entrée et
en sortie.


Pour débugger un code, une première étape peut être de désactiver toute optimisation
ou obfuscation, afin de travailler sur un code machine le plus proche possible du
code source. Cependant, dans certains cas, le bug détecté cessera d'appartaitre une
fois ces options désactivées. Dans ce cas, il peut s'agir d'un bug à l'intérieur d'une
passe d'optimisation ou d'obfuscation, et il relève donc des développeurs du compilateur
de le résoudre. Mais il peut également s'agir d'un bug dans le code source qui ne se
manifeste que lorsqu'il interagit avec certainse optimisations et/ou obfuscations.

Dans les deux cas, pour identifier le bug, accéder à l'histoire des instructions
pour mieux comprendre comment chaque instruction du code machine a été formée à partir
du code source serait un atout, à la fois pour l'utilisateur du compilateur pour l'aider
à identifier le bug, et pour le développeur du compilateur, pour l'aider dans le processus
de debugging du compilateur lui-même, en particulier lorsque le code produit par le compilateur
n'est pas correct.

---

Dans cette présentation, je souhaite présenter le problème détaillé ci-dessus, présenter
les travaux que j'ai effectué sur le compilateur LLVM pour tracer les transformations,
puis présenter deux cas d'usages-type de bugs pour lesquels la trace produite peut faciliter
le processus de debug.

### 6 - Temps de discussion.

**Benoit Combemale, Steven Costiou**
