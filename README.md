# Trio

**Prier. Contempler. Guérir.**
*Pray. Contemplate. Heal.*

Trio est un ensemble de trois applications web (PWA) autonomes, sans backend, sans compte, dont les données ne quittent jamais l'appareil. Chacune peut être utilisée seule — mais ensemble, elles forment un chemin :

```
   PLENIEL                    SELAH                      EMMAÜS
   journal de prière   →   pause contemplative   →   méditation de guérison
   (tu déposes)             (tu relies)                (tu reçois)
```

## Le concept

**[Pléniel](../pleniel)** est l'endroit où tu déposes ce que tu portes — tes prières, actives ou exaucées, classées par catégorie, accompagnées de versets et de chants pour t'accompagner dans le temps de prière. Le nom vient de *Peniel* (Genèse 32:30) : le lieu où Jacob a rencontré Dieu dans la nuit, après une lutte. Chaque prière déposée est ce même seuil.

**[Selah](../selah)** — mot hébreu des Psaumes signifiant une pause, une respiration au milieu du chant — reprend ce que tu as déposé dans Pléniel et prend le temps de le relire. Pour chaque prière : un verset, un ancrage théologique, et une *cognition positive* — une vérité que tu peux tenir dans la main quand la prière elle-même est encore un combat. Selah donne aussi à voir : tendances, catégories, constance dans le temps — un miroir doux sur ta vie de prière.

**[Emmaüs](../emmaus)** — du nom de la route où deux disciples, marchant dans le chagrin, ont reconnu le Christ à leurs côtés (Luc 24) — reçoit les cognitions positives préparées par Selah et les met au service de séances guidées d'EMDR (*Eye Movement Desensitization and Reprocessing*), avec tapping bilatéral et voix. Sa devise : *Il restaure mon âme* (Psaume 23:3). C'est le lieu où ce qui a été nommé et relu peut enfin être porté vers la guérison.

## Pourquoi trois applications séparées, et pas une seule ?

Parce que chaque étape demande une présence différente : déposer n'est pas la même chose que relire, et relire n'est pas la même chose que guérir. Séparer les outils protège chaque temps — et permet à chacun d'exister aussi seul, pour qui n'a besoin que d'un journal de prière, ou que d'un espace de méditation.

Le pont entre les trois est volontairement simple et entièrement local : Pléniel n'exporte rien automatiquement ; Selah génère à la demande un export JSON (`selah-emmaus-AAAA-MM-JJ.json`) à partir des prières de Pléniel, prêt à être relu dans Emmaüs. Aucune donnée ne transite par un serveur.

## Les trois dépôts

| App | Rôle | Dépôt |
|---|---|---|
| 🕯️ Pléniel | Journal de prière — versets, chants, minuteur, statistiques | [`pleniel`](../pleniel) |
| 🕊️ Selah | Contemplation — verset + cognition positive par prière, tableau de bord | [`selah`](../selah) |
| 🌿 Emmaüs | Méditation de guérison — séances EMDR guidées, tapping bilatéral, voix | [`emmaus`](../emmaus) |

Chaque application est un fichier HTML autonome (+ manifest/service worker pour l'installation en PWA), hébergeable gratuitement sur GitHub Pages, Netlify ou Vercel. Aucune dépendance serveur, aucune donnée envoyée à un tiers — hormis un appel optionnel à l'API ElevenLabs pour la voix dans Emmaüs, et à l'API Anthropic si tu actives l'assistance IA dans Selah/Pléniel.

---

*Trio est un projet personnel, développé avec l'aide de Claude (Anthropic), pour un usage privé de prière et de guérison intérieure.*
