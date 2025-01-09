# **SFX Commands Guide**

Vayl Bot's **SFX Commands** feature allows users to create and manage an unlimited number of sound commands, all sourced from files stored locally on their computer. This feature provides great flexibility for enhancing viewer engagement with custom sound effects.

---

## **Structure of `sfx.yml`**

The `sfx.yml` file is located within the `configuration` folder. Below is the structure of a typical SFX configuration:

```yaml
enabled: true
global-cooldown: 0
sounds:
  <command_name>:
    sound: <sound_filename>
    streamer-only: <true_or_false>
    sub-only: <true_or_false>
    mod-only: <true_or_false>
    vip-only: <true_or_false>
    cooldown:
      user: <time_in_seconds>
      global: <time_in_seconds>
```

---

### **Fields Explained**

1. **`enabled`**:
   - Acts as a global toggle for SFX commands.
   - If `true`, all SFX commands are enabled.
   - If `false`, no SFX commands will function.

2. **`global-cooldown`**:
   - A global cooldown (in seconds) applied to all SFX commands. No SFX command can be used during this time.

3. **`sounds`**:
   - The base directory for all SFX commands. Each sub-entry represents an individual SFX command.

4. **`<command_name>`**:
   - The identifier for the SFX command. This is also the command users type in chat to trigger the sound effect.

5. **`sound`**:
   - The filename (without extension) of the sound file to be played.
   - Vayl automatically checks for the file within the `sounds` folder in the `data` directory and recognizes common file extensions (e.g., `.mp3`, `.wav`).

6. **Access Restrictions**:
   - **`streamer-only`**: If `true`, only the streamer can use the command.
   - **`sub-only`**: If `true`, only subscribers can use the command.
   - **`mod-only`**: If `true`, only moderators can use the command.
   - **`vip-only`**: If `true`, only VIPs can use the command.

7. **`cooldown`**:
   - **`user`**: The time (in seconds) a specific user must wait before using the command again.
   - **`global`**: The time (in seconds) that must pass before anyone can use the command again.

---

## **Example Configuration**

Here’s an example configuration for an SFX command called `ayy`:

```yaml
enabled: true
global-cooldown: 0
sounds:
  ayy:
    sound: ayy
    streamer-only: false
    sub-only: false
    mod-only: false
    vip-only: false
    cooldown:
      user: 10
      global: 10
```

### **Explanation**
- **Command Name**: `ayy`
  - Users type `!ayy` in chat to trigger this sound effect.
- **Sound File**: `ayy`
  - The bot plays the file named `ayy.mp3` or `ayy.wav` (or another supported format) located in the `sounds` folder under the `data` directory.
- **Access**: Open to all users.
- **Cooldowns**:
  - **User Cooldown**: 10 seconds.
  - **Global Cooldown**: 10 seconds.

---

## **Best Practices**

1. **Organize Sound Files**:
   - Store all sound files in the `sounds` folder inside the `data` directory.
   - Use consistent and descriptive filenames for easier management.

2. **Use Cooldowns Wisely**:
   - Set appropriate user and global cooldowns to prevent spamming.
   - Use the `global-cooldown` setting for additional control.

3. **Restrict Commands**:
   - Use `streamer-only`, `mod-only`, `sub-only`, or `vip-only` settings to limit access to specific commands as needed.

4. **Test Sounds**:
   - Verify that all sound files are accessible and working properly before going live.

---

For more information on how to configure other actions, see the [Actions Guide](actions.md).

