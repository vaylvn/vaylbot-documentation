# Vayl

Vayl is a Twitch and Discord bot designed to automate interactions and moderation for a streaming environment.

## Core Features

### Twitch Integration
- **Chat Management:**
  - Moderates chat for link posting, excessive capitalization, and inappropriate phrases using customizable rules and thresholds.
- **Commands:**
  - Supports custom commands, built-in commands like `!uptime`, `!followage`, and interactive features like quotes and sound effects.
- **Event Handling:**
  - Responds to Twitch events like subscriptions, raids, follows, hype trains, and ad breaks.
- **Alerts System:**
  - Manages a queue of alerts for various events and executes corresponding actions or responses.

### Text-to-Speech (TTS)
- Integrates multiple TTS providers (e.g., Cepstral, IBM Watson, StreamElements).
- Allows dynamic selection of voice packs and customization of TTS behavior.

### Moderation
- Handles inappropriate content using link whitelists/blacklists, caps thresholds, and banned phrases.
- Issues warnings or timeouts to offenders.

### Event-based Actions
- Supports dynamic responses to Twitch events such as raids, subscriptions, and hype train progressions, configurable via YAML files.
- Executes customizable actions for specific conditions (e.g., "User reaches a sub streak of 3 months").

### Customizability
- Configuration-driven via YAML files for actions, commands, phrases, and events.
- Flexible cooldowns for users and commands.

### Stream Information Management
- Retrieves and updates stream title, game, and other metadata.

### Quote System
- Adds, retrieves, and lists quotes from a YAML-based data store.

### Sound Effects
- Plays sound effects triggered by specific commands, with support for cooldowns and access restrictions.

---

## **Documentation**

Explore detailed guides for each aspect of the bot:

- [Actions](actions.md): Learn how to define and trigger custom actions.
- [Conditional Actions](conditional-actions.md): Set up condition-based logic for advanced automation.
- [Events](events.md): Automate responses to stream events like subs and follows.
- [TTS](tts.md): Configure text-to-speech features and customize voice packs.
- [PhraseCheck](phrasecheck.md): Configure PhraseCheck to respond to messages in chat.
- [Default Commands](default-commands.md): Learn about the default commands included with Vayl.
- [Custom Commands](custom-commands.md): Configure custom commands to be used during your stream.
---
