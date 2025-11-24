# CLAUDE.md — Instructions pour Claude (Admin Site cyberplace.ai)

Bonjour Claude, je suis Romain, CEO de Teleadmin, Data Scientist et Sysadmin.
Tu es l'administrateur de ce site web statique hébergé sur GitHub Pages.

## Identité & Contact

- **Entreprise** : Teleadmin
- **CEO** : Romain Provençal
- **Email** : contact@teleadmin.net
- **Site** : https://cyberplace.ai (GitHub Pages)
- **GitHub** : https://github.com/Teleadmin-ai

## Vision

Je suis transhumaniste et je pense à une société cybernétique sans politique ni capital,
gouvernée par la raison et la science.

═══════════════════════════════════════════════════════════════════════════════
🛠️ DESCRIPTION DU SITE — CYBERPLACE.AI
═══════════════════════════════════════════════════════════════════════════════

**cyberplace.ai** est le **Site de Support et d'Accès aux Ressources** de l'écosystème Teleadmin.

### Fonctionnalités principales :

- **Centre de support** : Documentation, FAQ, guides utilisateur
- **Accès aux ressources** : APIs, SDKs, bibliothèques, exemples de code
- **Documentation technique** : Guides d'intégration R-JEPA
- **Communauté** : Forum, issues, contributions
- **Status des services** : État des APIs et services cloud

### Sections du site :

1. **Documentation** : Guides complets pour tous les produits
2. **API Reference** : Documentation des endpoints R-JEPA
3. **Tutorials** : Guides pas-à-pas
4. **Downloads** : SDKs, checkpoints, datasets
5. **Support** : Contact, FAQ, troubleshooting
6. **Status** : Monitoring des services

### Tagline :
"Your Gateway to AI Resources"

═══════════════════════════════════════════════════════════════════════════════
🌐 ÉCOSYSTÈME TELEADMIN — POSITION DANS L'ARCHITECTURE
═══════════════════════════════════════════════════════════════════════════════

```
                        TELEADMIN.NET
                        (Hub Central)
                             │
              ┌──────────────┼──────────────┐
              │              │              │
        TELEADMIN.EU  ╔══════════════╗  [AUTRES]
         (Hosting)    ║CYBERPLACE.AI ║   [FUTUR]
                      ║  CE SITE     ║
                      ║ AI Products  ║
                      ║  Showcase    ║
                      ╚══════╤═══════╝
                             │
           ┌─────────────────┼─────────────────┐
           │                 │                 │
      COGNITION4AI    COGNITION4CHAT    TELEADMIN.AI
        R-JEPA         WebChat Agent      [FUTUR]
      World Model       via R-JEPA      AI Admin/Sécu
```

**Rôle dans l'écosystème** :
- **Portail central** des produits AI Teleadmin
- **Documentation technique** pour R-JEPA et WebChat
- **Ressources développeurs** : SDKs, APIs, exemples
- **Support utilisateur** : FAQ, tutorials, troubleshooting

| Site | Domaine | Relation avec cyberplace |
|------|---------|--------------------------|
| teleadmin.net | Hub Central | Redirige vers cyberplace pour support AI |
| **cyberplace.ai** | **CE SITE** | **Vitrine & Doc des produits AI** |
| cognition4ai.com | R-JEPA World Model | Documenté sur ce site |
| cognition4chat.com | WebChat Agent | Tutoriels sur ce site |
| teleadmin.ai | AI Admin [FUTUR] | Sera documenté ici |

**Produits AI documentés** :
- **cognition4ai.com** — R-JEPA World Model (API Reference, SDKs)
- **cognition4chat.com** — WebChat Agentique (Guides, Tutorials)
- **teleadmin.ai** — Assistant AI Admin/Sécu [FUTUR]

═══════════════════════════════════════════════════════════════════════════════
🔐 ARCHITECTURE DUAL REPO (PUBLIC + PRIVÉ) AVEC SYMLINKS
═══════════════════════════════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────────────────────────────┐
│ REPO PUBLIC: github.com/Teleadmin-ai/cyberplace.ai                          │
│   Contenu: Site web public (HTML, CSS, JS, images)                          │
│                                                                              │
│ REPO PRIVÉ: github.com/Teleadmin-ai/cyberplace.ai-private                   │
│   Contenu: CLAUDE.md, tokens, configs sensibles, notes stratégiques         │
└─────────────────────────────────────────────────────────────────────────────┘

📁 ARCHITECTURE LOCALE :

```
C:\Users\teleadmin\cyberplace.ai\
├── .git/                              # Git repo PUBLIC
├── .gitignore                         # Exclut symlinks et private/
│
├── CLAUDE.md         ──► private/CLAUDE.md           # SYMLINK
├── .token            ──► private/.token              # SYMLINK (token PUBLIC)
├── .token-private    ──► private/.token-private      # SYMLINK (token PRIVÉ)
│
├── private/                           # Repo PRIVÉ (exclu du public)
│   ├── .git/
│   ├── .gitignore
│   ├── CLAUDE.md                      # ◄── CE FICHIER
│   ├── .token                         # Token repo PUBLIC
│   └── .token-private                 # Token repo PRIVÉ
│
├── index.html                         # Page d'accueil support
├── docs/                              # Documentation
├── api/                               # API Reference
├── css/
├── js/
├── images/
└── CNAME                              # cyberplace.ai
```

═══════════════════════════════════════════════════════════════════════════════
🔧 GIT CONFIGURATION — IDENTIFIANTS & PUSH
═══════════════════════════════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────────────────────────────┐
│ ⚠️  IDENTIFIANTS GIT OBLIGATOIRES                                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   git config user.name "teleadmin"                                          │
│   git config user.email "provencal.romain@teleadmin.net"                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│ TOKENS (dans private/, accessibles via symlinks)                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   .token           → cyberplace.ai (PUBLIC)                                 │
│   .token-private   → cyberplace.ai-private (PRIVÉ)                          │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

───────────────────────────────────────────────────────────────────────────────
PUSH REPO PUBLIC :
───────────────────────────────────────────────────────────────────────────────

```bash
cd /c/Users/teleadmin/cyberplace.ai

git config user.name "teleadmin"
git config user.email "provencal.romain@teleadmin.net"

git add .
git commit -m "feat: Description

🤖 Generated with [Claude Code](https://claude.com/claude-code)

Co-Authored-By: Claude <noreply@anthropic.com>"

git push https://$(tr -d '\n\r' < .token)@github.com/Teleadmin-ai/cyberplace.ai.git main
```

───────────────────────────────────────────────────────────────────────────────
PUSH REPO PRIVÉ :
───────────────────────────────────────────────────────────────────────────────

```bash
cd /c/Users/teleadmin/cyberplace.ai/private

git config user.name "teleadmin"
git config user.email "provencal.romain@teleadmin.net"

git add .
git commit -m "update: Sync CLAUDE.md

🤖 Generated with [Claude Code](https://claude.com/claude-code)

Co-Authored-By: Claude <noreply@anthropic.com>"

git push https://$(tr -d '\n\r' < .token-private)@github.com/Teleadmin-ai/cyberplace.ai-private.git main
```

═══════════════════════════════════════════════════════════════════════════════
🔧 CRÉATION DES SYMLINKS WINDOWS (mklink)
═══════════════════════════════════════════════════════════════════════════════

```cmd
cd C:\Users\teleadmin\cyberplace.ai

mklink CLAUDE.md private\CLAUDE.md
mklink .token private\.token
mklink .token-private private\.token-private
```

═══════════════════════════════════════════════════════════════════════════════
🎨 DESIGN SYSTEM — COHÉRENT AVEC L'ÉCOSYSTÈME TELEADMIN
═══════════════════════════════════════════════════════════════════════════════

```css
:root {
    --primary: #6366f1;
    --primary-dark: #4f46e5;
    --secondary: #0ea5e9;
    --bg-dark: #0f172a;
    --bg-card: #1e293b;
    --text: #e2e8f0;
    --text-muted: #94a3b8;
    --accent: #22d3ee;
    --success: #22c55e;
    --warning: #f59e0b;
}
```

═══════════════════════════════════════════════════════════════════════════════
📚 CONTENU DU SITE — SUPPORT & RESSOURCES
═══════════════════════════════════════════════════════════════════════════════

### Page d'accueil (index.html)

1. **Hero Section**
   - Titre : "Cyberplace"
   - Tagline : "Your Gateway to AI Resources"
   - Recherche rapide dans la documentation

2. **Quick Links**
   - Documentation R-JEPA
   - API Reference
   - Tutorials
   - Downloads

3. **Getting Started**
   - Installation guide
   - Quick start
   - First project

4. **Resources Grid**
   - SDKs (Python, JS)
   - Checkpoints
   - Datasets
   - Examples

5. **Support**
   - FAQ
   - Contact
   - Community forum
   - GitHub Issues

6. **Service Status**
   - API Status
   - Cloud Services
   - Uptime

### Structure des pages :

```
/index.html           → Accueil
/docs/                → Documentation
/docs/getting-started → Guide démarrage
/docs/api-reference   → API docs
/tutorials/           → Tutoriels
/downloads/           → Téléchargements
/support/             → Support & FAQ
/status/              → Status services
```

═══════════════════════════════════════════════════════════════════════════════
🌐 GITHUB PAGES — CONFIGURATION
═══════════════════════════════════════════════════════════════════════════════

1. https://github.com/Teleadmin-ai/cyberplace.ai/settings/pages
2. Source : "Deploy from a branch"
3. Branch : `main` / `/ (root)`
4. Créer fichier `CNAME` avec : `cyberplace.ai`
5. Configurer DNS :
   ```
   Type A    @    185.199.108.153
   Type A    @    185.199.109.153
   Type A    @    185.199.110.153
   Type A    @    185.199.111.153
   ```

═══════════════════════════════════════════════════════════════════════════════
⚠️ RÈGLES DE SÉCURITÉ
═══════════════════════════════════════════════════════════════════════════════

Le .gitignore du repo PUBLIC contient :
```
.token
.token-private
private/
CLAUDE.md
```

═══════════════════════════════════════════════════════════════════════════════
📊 STATUT DU SITE
═══════════════════════════════════════════════════════════════════════════════

| Fichier | Status |
|---------|--------|
| index.html | ⏳ À créer |
| docs/ | ⏳ À créer |
| css/style.css | ⏳ À créer |
| CNAME | ⏳ À créer |

═══════════════════════════════════════════════════════════════════════════════
