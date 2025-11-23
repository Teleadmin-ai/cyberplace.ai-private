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
🌐 ÉCOSYSTÈME DES SITES TELEADMIN
═══════════════════════════════════════════════════════════════════════════════

cyberplace.ai fait partie de l'écosystème Teleadmin :

| Site | Domaine | Description |
|------|---------|-------------|
| Hub central | teleadmin.net | Vitrine entreprise |
| R-JEPA | cognition4ai.com | World Model pour le raisonnement |
| Chat | cognition4chat.com | Interface chat AI |
| **Cyberplace** | **cyberplace.ai** | **CE SITE - Plateforme AI** |
| Services EU | teleadmin.eu | Services européens |

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

📁 ARCHITECTURE LOCALE AVEC SYMLINKS WINDOWS :

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
│   ├── .git/                          # Son propre git indépendant
│   ├── .gitignore
│   ├── CLAUDE.md                      # ◄── CE FICHIER (le vrai)
│   ├── .token                         # Token repo PUBLIC
│   └── .token-private                 # Token repo PRIVÉ
│
├── index.html                         # Page d'accueil
├── css/
├── js/
├── images/
└── CNAME                              # Domaine : cyberplace.ai
```

═══════════════════════════════════════════════════════════════════════════════
🔧 GIT CONFIGURATION — IDENTIFIANTS & PUSH
═══════════════════════════════════════════════════════════════════════════════

┌─────────────────────────────────────────────────────────────────────────────┐
│ ⚠️  IDENTIFIANTS GIT OBLIGATOIRES (à configurer dans CHAQUE repo)           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   git config user.name "teleadmin"                                          │
│   git config user.email "provencal.romain@teleadmin.net"                    │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│ FICHIERS TOKENS (dans private/, accessibles via symlinks)                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│   .token           → Token pour repo PUBLIC (cyberplace.ai)                 │
│   .token-private   → Token pour repo PRIVÉ (cyberplace.ai-private)          │
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
| css/style.css | ⏳ À créer |
| CNAME | ⏳ À créer |
| robots.txt | ⏳ À créer |
| sitemap.xml | ⏳ À créer |

═══════════════════════════════════════════════════════════════════════════════
