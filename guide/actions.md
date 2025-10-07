# **Actions**

Actions define what Vayl should do when triggered by an event.

All actions follow the format:
```yaml
[action] | <required_arg> | [optional_arg]
```

**Syntax Key:**
- `<arg>` → Required argument  
- `[arg]` → Optional argument  
- Arguments are separated by vertical bars (`|`)  
- All actions support the [Tag System](tags.md) — e.g., `[user]`, `[counter:name]`, `[text:name]`, etc.

---

## 🧩 **OBS Integration**

<details><summary><strong>obs:scene</strong> — Switch to a specific OBS scene</summary>

```yaml
obs:scene | <scene_name>
```
Example:
```yaml
- obs:scene | Starting Soon
```
</details>

<details><summary><strong>obs:show</strong> — Show a specific OBS source</summary>

```yaml
obs:show | <source_name>
```
Example:
```yaml
- obs:show | Webcam
```
</details>

<details><summary><strong>obs:hide</strong> — Hide a specific OBS source</summary>

```yaml
obs:hide | <source_name>
```
Example:
```yaml
- obs:hide | AlertBox
```
</details>

<details><summary><strong>obs:toggle</strong> — Toggle visibility of an OBS source</summary>

```yaml
obs:toggle | <source_name>
```
Example:
```yaml
- obs:toggle | ChatOverlay
```
</details>

<details><summary><strong>obs:label</strong> — Update label text or color</summary>

```yaml
obs:label | <source_name> | <text> | [color]
```
Example:
```yaml
- obs:label | StreamTitle | [counter:subs] Subs | #FFFFFF
```
</details>

<details><summary><strong>obs:mediafile</strong> — Change media file for a source</summary>

```yaml
obs:mediafile | <source_name> | <file_path>
```
Example:
```yaml
- obs:mediafile | VideoSource | media/intro.mp4
```
</details>

<details><summary><strong>obs:image</strong> — Change the image file for an image source</summary>

```yaml
obs:image | <source_name> | <file_path>
```
Example:
```yaml
- obs:image | Overlay | images/new_banner.png
```
</details>

<details><summary><strong>obs:media</strong> — Control media source playback</summary>

```yaml
obs:media | <source_name> | <play/pause/stop/restart/next/previous/position>
```
Example:
```yaml
- obs:media | IntroVideo | play
```
</details>

<details><summary><strong>obs:slideshow</strong> — Control a slideshow source</summary>

```yaml
obs:slideshow | <source_name> | <play/pause/stop/restart/next/previous/position>
```
Example:
```yaml
- obs:slideshow | Screens | next
```
</details>

<details><summary><strong>obs:filter</strong> — Enable or disable a source filter</summary>

```yaml
obs:filter | <source_name> | <filter_name> | <enabled/disabled>
```
Example:
```yaml
- obs:filter | Camera | Blur | enabled
```
</details>

<details><summary><strong>obs:audio</strong> — Adjust an audio source’s volume</summary>

```yaml
obs:audio | <source_name> | <percentage> | <steps> | <duration>
```
Example:
```yaml
- obs:audio | Music | 50 | 5 | 2
```
</details>

---

## 💬 **Chat & Moderation**

<details><summary><strong>chat</strong> — Send a message in chat</summary>

```yaml
chat | <message>
```
Example:
```yaml
- chat | Hello [user]!
```
</details>

<details><summary><strong>announce</strong> — Send a Twitch announcement</summary>

```yaml
announce | <message> | [blue/green/orange/purple/primary]
```
Example:
```yaml
- announce | Stream starting soon! | orange
```
</details>

<details><summary><strong>vip</strong> — Add or remove a Twitch VIP</summary>

```yaml
vip | <add/remove> | <username>
```
Example:
```yaml
- vip | add | SomeUser
```
</details>

<details><summary><strong>timeout</strong> — Timeout a user</summary>

```yaml
timeout | <user> | <duration> | [reason]
```
Example:
```yaml
- timeout | [user] | 300 | Spam detected
```
</details>

<details><summary><strong>createclip</strong> — Create a Twitch clip</summary>

```yaml
createclip
```
Example:
```yaml
- createclip
```
</details>

<details><summary><strong>addmarker</strong> — Add a stream marker</summary>

```yaml
addmarker
```
Example:
```yaml
- addmarker
```
</details>

---

## 🔢 **Variables**

<details><summary><strong>text</strong> — Modify text variables</summary>

```yaml
text | <variable_name> | <set/append> | <text>
```
Example:
```yaml
- text | status | set | Stream is live!
```
</details>

<details><summary><strong>counter</strong> — Modify numeric counters</summary>

```yaml
counter | <variable_name> | <set/increase/decrease/multiply/divide> | <amount>
```
Example:
```yaml
- counter | deaths | increase | 1
```
</details>

<details><summary><strong>counter2</strong> — Modify counters using an equation</summary>

```yaml
counter2 | <variable_name> | <equation>
```
Example:
```yaml
- counter2 | points | value * 2 + 10
```
</details>

<details><summary><strong>boolean</strong> — Set a boolean variable</summary>

```yaml
boolean | <variable_name> | <true/false>
```
Example:
```yaml
- boolean | isActive | true
```
</details>

<details><summary><strong>table</strong> — Modify a table variable</summary>

```yaml
table | <table_name> | <entry_name> | <entry_value>
```
Example:
```yaml
- table | stats | accuracy | 97%
```
</details>

<details><summary><strong>list</strong> — Modify list variables</summary>

```yaml
list | <variable_name> | <clear/add/remove> | [text]
```
Example:
```yaml
- list | viewers | add | [user]
```
</details>

---

## ⚙️ **Utility**

<details><summary><strong>playsound</strong> — Play a sound by name</summary>

```yaml
playsound | <sound_name>
```
Example:
```yaml
- playsound | alert.wav
```
</details>

<details><summary><strong>wait</strong> — Pause execution</summary>

```yaml
wait | <seconds>
```
Example:
```yaml
- wait | 5
```
</details>

<details><summary><strong>console</strong> — Print text to the Vayl console</summary>

```yaml
console | <message>
```
Example:
```yaml
- console | Event triggered successfully
```
</details>

<details><summary><strong>cmd</strong> — Execute a system command</summary>

```yaml
cmd | <command>
```
Example:
```yaml
- cmd | echo Hello World
```
</details>

<details><summary><strong>actionpack</strong> — Run a predefined action pack</summary>

```yaml
actionpack | <name>
```
Example:
```yaml
- actionpack | on_sub
```
</details>

---

## 🧠 **Advanced / System**

<details><summary><strong>conditional</strong> — Trigger a conditional</summary>

```yaml
conditional | <conditional_name>
```
Example:
```yaml
- conditional | hype_start
```
**Learn more:** See the [Conditionals Reference](conditionals.md) for detailed usage.
</details>

<details><summary><strong>webhook</strong> — Trigger a webhook</summary>

```yaml
webhook | <webhook_name>
```
Example:
```yaml
- webhook | discord_notify
```
</details>

<details><summary><strong>tts</strong> — Speak text using Text-to-Speech</summary>

```yaml
tts | <voice> | <message> | [true/false] | [character_limit]
```
Example:
```yaml
- tts | Ivy | [user_input] | true | 500
```
</details>
