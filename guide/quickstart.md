# **Vayl Bot Quickstart Guide**

Welcome to Vayl Bot! Follow this guide to quickly get your bot up and running.

---

## **Step 1: Download Vayl Bot**

1. Go to the [Vayl Bot GitHub Releases Page](https://github.com/vaylvn/vaylbot/releases).
2. Download the latest ZIP file.
3. Extract the contents to a folder on your computer.

---

## **Step 2: Configuration**

1. Navigate to the `configuration` folder and open `configuration.yml` in a text editor of your choice.
2. Update the following fields:
   - **`connected-account`**: Set this to your Twitch username.
     ```yaml
     connected-account: your-twitch-username
     ```
   - **`obs-password`** *(optional)*: If you want OBS integration, set this to your OBS WebSocket password.
     ```yaml
     obs-password: your-obs-password
     ```
   - **`bug-auto-report`**: Enable or disable automatic bug reporting.
     ```yaml
     bug-auto-report: true
     ```
     **Note**: If enabled, a copy of the error log will be sent directly to the developer (viewable only by the developer). Be aware that the error log may include file paths, which could contain your username or other identifying information depending on your PC setup.

---

## **Step 3: Run Vayl Bot**

1. Double-click `vayl.exe` to start the bot.
2. A webpage will open, prompting you to grant access for Vayl Bot to your Twitch account. This is required to:
   - Access events like subs, follows, raids, etc.
   - Interact with chat.
   - Use other Twitch API scopes.
3. Complete the authorization process.

---

## **Step 4: Configure as Needed**

After initial setup, you can:
- Close the Vayl console.
- Adjust additional configurations in `configuration.yml` or other files.

### **Reloading Configurations**

- **Restart Required**: Modifying certain configurations, such as registering new commands, phrases for PhraseCheck, or ModerationData, requires you to restart Vayl.
- **Dynamic Updates**: Action lists are dynamically loaded and do not require a restart. You can modify them on the fly.

To reload configurations without restarting:
- Use the command `!reload` in the chat.

---

## **Next Steps**

Once Vayl Bot is running, explore the following guides:
- [Actions Guide](actions.md): Set up and customize bot actions.
- [Conditional Actions](conditional-actions.md): Use advanced logic for triggers.
- [Events Guide](events.md): Automate responses to Twitch events.
- [TTS Guide](tts.md): Configure text-to-speech for engaging interactions.
- [PhraseCheck](phrasecheck.md): Configure PhraseCheck to respond to messages in chat.

Enjoy your fully customizable chatbot experience!

