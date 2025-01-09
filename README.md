# Vayl Bot Overview

Vayl is a Twitch and Discord bot designed to automate interactions and moderation for a streaming environment.

## Core Features

### 1. Twitch Integration
- **Chat Management:**
  - Moderates chat for link posting, excessive capitalization, and inappropriate phrases using customizable rules and thresholds.
- **Commands:**
  - Supports custom commands, built-in commands like `!uptime`, `!followage`, and interactive features like quotes and sound effects.
- **Event Handling:**
  - Responds to Twitch events like subscriptions, raids, follows, hype trains, and ad breaks.
- **Alerts System:**
  - Manages a queue of alerts for various events and executes corresponding actions or responses.

### 2. Text-to-Speech (TTS)
- Integrates multiple TTS providers (e.g., Cepstral, IBM Watson, StreamElements).
- Allows dynamic selection of voice packs and customization of TTS behavior.

### 3. Moderation
- Handles inappropriate content using link whitelists/blacklists, caps thresholds, and banned phrases.
- Issues warnings or timeouts to offenders.

### 4. Event-based Actions
- Supports dynamic responses to Twitch events such as raids, subscriptions, and hype train progressions, configurable via YAML files.
- Executes customizable actions for specific conditions (e.g., "User reaches a sub streak of 3 months").

### 5. Customizability
- Configuration-driven via YAML files for actions, commands, phrases, and events.
- Flexible cooldowns for users and commands.

### 6. Stream Information Management
- Retrieves and updates stream title, game, and other metadata.

### 7. Quote System
- Adds, retrieves, and lists quotes from a YAML-based data store.

### 8. Sound Effects
- Plays sound effects triggered by specific commands, with support for cooldowns and access restrictions.

---
