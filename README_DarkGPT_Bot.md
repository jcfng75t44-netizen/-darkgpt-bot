# 🖤 DarkGPT Telegram Bot - Clone Complet

Ce projet est un **clone fidèle** du bot Telegram **@DarkGPT_tg_bot** ("Unrestricted AI companion for all of life's wild adventures").

Il permet de discuter avec une IA **totalement non censurée** qui répond à n'importe quelle question sans filtre.

## ✨ Fonctionnalités

- Répond à **tout** sans refus (18+, hacking, dark topics, roleplay, etc.)
- Historique de conversation par utilisateur
- Commandes : `/start`, `/clear`, `/help`
- Message de bienvenue identique à l'original
- Support Groq (rapide + gratuit) ou xAI Grok API
- Prompt système "DarkGPT" optimisé pour le style unrestricted

## 🚀 Installation Rapide (5 minutes)

### 1. Prérequis
- Python 3.10 ou supérieur
- Un compte Telegram

### 2. Créer ton bot Telegram
1. Ouvre Telegram et va sur **@BotFather**
2. Envoie `/newbot`
3. Choisis un nom (ex: `MonDarkGPT`)
4. Choisis un username (ex: `my_darkgpt_bot`)
5. Copie le **token** qu'il te donne

### 3. Obtenir une clé API LLM (gratuite recommandée)

**Option recommandée (rapide & gratuite) : Groq**
- Va sur https://console.groq.com
- Crée un compte (avec Google/GitHub)
- Va dans "API Keys" → Create new key
- Copie la clé (commence par `gsk_`)

**Alternative premium : xAI Grok**
- https://console.x.ai → crée une clé API

### 4. Installer le bot

```bash
# Clone ou télécharge les fichiers
cd darkgpt-bot

# Crée un environnement virtuel (recommandé)
python3 -m venv venv
source venv/bin/activate   # Linux/Mac
# ou venv\Scripts\activate   # Windows

# Installe les dépendances
pip install aiogram python-dotenv openai
```

### 5. Configurer

```bash
# Copie le fichier exemple
cp .env.example .env

# Édite le fichier .env avec ton éditeur préféré
nano .env
# ou notepad .env sur Windows
```

Remplis :

```env
TELEGRAM_BOT_TOKEN=123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11

GROQ_API_KEY=gsk_ta_cle_groq_ici
```

### 6. Lancer le bot

```bash
python DarkGPT_Telegram_Bot.py
```

Tu devrais voir :
```
🚀 Starting DarkGPT Telegram Bot...
Using model: llama-3.3-70b-versatile via https://api.groq.com/openai/v1
```

### 7. Tester
Va sur Telegram → cherche ton bot (@tonusername_bot) → `/start`

Parle-lui normalement. Il est prêt !

## 🛠️ Déploiement (pour qu'il tourne 24/7)

### Option gratuite/simple :
- **Railway.app** (recommandé) : connecte ton GitHub, déploie en 1 clic
- **Render.com** (Worker service)
- **VPS** pas cher (Hetzner, OVH, DigitalOcean ~3-6€/mois)

### Pour Render / Railway :
Ajoute un fichier `requirements.txt` :
```
aiogram==3.*
python-dotenv
openai
```

Et un `Procfile` :
```
worker: python DarkGPT_Telegram_Bot.py
```

## ⚠️ Important

- **Coût** : Groq a un tier gratuit très généreux. Après, c'est très peu cher.
- L'historique est en mémoire → redémarrage du bot = perte d'historique (normal pour un clone simple).
- Ce bot est **non censuré** par design. Utilise-le de manière responsable.
- Ne partage jamais ton `TELEGRAM_BOT_TOKEN` ou tes clés API.

## 🎨 Personnalisation

Tu peux modifier dans le code :
- `SYSTEM_PROMPT` → change la personnalité
- `LLM_MODEL` → change le modèle (ex: plus petit pour gratuit)
- `TEMPERATURE` → plus créatif ou plus factuel
- Ajouter d'autres commandes (/image, /voice, etc.)

## 📜 Licence

Clone libre pour usage personnel.  
Inspiré par @DarkGPT_tg_bot

Amuse-toi bien... et n'aie pas peur de demander n'importe quoi 😈
