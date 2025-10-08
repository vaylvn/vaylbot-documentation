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
- obs:scene | <scene_name>
```
</details>

<details><summary><strong>obs:show</strong> — Show an OBS source</summary>

```yaml
obs:show | <source>
```
Example:
```yaml
- obs:show | <source>
```
</details>

<details><summary><strong>obs:hide</strong> — Hide an OBS source</summary>

```yaml
obs:hide | <source>
```
Example:
```yaml
- obs:hide | <source>
```
</details>

<details><summary><strong>obs:toggle</strong> — Toggle visibility of an OBS source</summary>

```yaml
obs:toggle | <source>
```
Example:
```yaml
- obs:toggle | <source>
```
</details>

<details><summary><strong>obs:image</strong> — Change the image file for an image source</summary>

```yaml
obs:image | <source> | <file_path>
```
Example:
```yaml
- obs:image | <source> | <file_path>
```
</details>

<details><summary><strong>obs:label</strong> — Update a label’s text, color, or style</summary>

```yaml
obs:label | <source> | <text> | [color] | [size] | [font]
```
Example:
```yaml
- obs:label | <source> | <text> | [color] | [size] | [font]
```
</details>

<details><summary><strong>obs:mediafile</strong> — Change a media source’s file</summary>

```yaml
obs:mediafile | <source> | <file_path>
```
Example:
```yaml
- obs:mediafile | <source> | <file_path>
```
</details>

<details><summary><strong>obs:slideshow</strong> — Control a slideshow source</summary>

```yaml
obs:slideshow | <source> | <state>
```
Example:
```yaml
- obs:slideshow | <source> | <state>
```
</details>

<details><summary><strong>obs:filteron</strong> — Enable a source filter</summary>

```yaml
obs:filteron | <source> | <filter>
```
Example:
```yaml
- obs:filteron | <source> | <filter>
```
</details>

<details><summary><strong>obs:filteroff</strong> — Disable a source filter</summary>

```yaml
obs:filteroff | <source> | <filter>
```
Example:
```yaml
- obs:filteroff | <source> | <filter>
```
</details>

<details><summary><strong>obs:audio</strong> — Adjust an audio source’s volume</summary>

```yaml
obs:audio | <source> | <percentage> | <steps> | <duration>
```
Example:
```yaml
- obs:audio | <source> | <percentage> | <steps> | <duration>
```
</details>

---

## 💬 **Chat & Moderation**
<details><summary><strong>chat:message</strong> — Send a message in chat</summary>

```yaml
chat:message | <message>
```
Example:
```yaml
- chat:message | <message>
```
</details>

<details><summary><strong>chat:announce</strong> — Send a Twitch announcement</summary>

```yaml
chat:announce | <message>
```
Example:
```yaml
- chat:announce | <message>
```
</details>

<details><summary><strong>vip:add</strong> — Add a Twitch VIP</summary>

```yaml
vip:add | <username>
```
Example:
```yaml
- vip:add | <username>
```
</details>

<details><summary><strong>vip:remove</strong> — Remove a Twitch VIP</summary>

```yaml
vip:remove | <username>
```
Example:
```yaml
- vip:remove | <username>
```
</details>

<details><summary><strong>timeout</strong> — Timeout a user</summary>

```yaml
timeout | <username> | <duration> | [reason]
```
Example:
```yaml
- timeout | <username> | <duration> | [reason]
```
</details>

<details><summary><strong>stream:clip</strong> — Create a Twitch clip</summary>

```yaml
stream:clip
```
Example:
```yaml
- stream:clip
```
</details>

<details><summary><strong>stream:marker</strong> — Add a stream marker</summary>

```yaml
stream:marker
```
Example:
```yaml
- stream:marker
```
</details>

<details><summary><strong>stream:raid</strong> — Raid another streamer</summary>

```yaml
stream:raid | <username>
```
Example:
```yaml
- stream:raid | <username>
```
</details>

<details><summary><strong>redeem:create</strong> — Create a channel point reward</summary>

```yaml
redeem:create | <name>
```
Example:
```yaml
- redeem:create | <name>
```
</details>

<details><summary><strong>redeem:enable</strong> — Enable a channel point reward</summary>

```yaml
redeem:enable | <name>
```
Example:
```yaml
- redeem:enable | <name>
```
</details>

<details><summary><strong>redeem:disable</strong> — Disable a channel point reward</summary>

```yaml
redeem:disable | <name>
```
Example:
```yaml
- redeem:disable | <name>
```
</details>

<details><summary><strong>redeem:toggle</strong> — Toggle a channel point reward</summary>

```yaml
redeem:toggle | <name>
```
Example:
```yaml
- redeem:toggle | <name>
```
</details>

---

## 🔢 **Variables**
<details><summary><strong>text:set</strong> — Set a text variable</summary>

```yaml
text:set | <name> | <text>
```
Example:
```yaml
- text:set | <name> | <text>
```
</details>

<details><summary><strong>text:prepend</strong> — Prepend text to a variable</summary>

```yaml
text:prepend | <name> | <text>
```
Example:
```yaml
- text:prepend | <name> | <text>
```
</details>

<details><summary><strong>text:append</strong> — Append text to a variable</summary>

```yaml
text:append | <name> | <text>
```
Example:
```yaml
- text:append | <name> | <text>
```
</details>

<details><summary><strong>text:clear</strong> — Clear text from a variable</summary>

```yaml
text:clear | <name>
```
Example:
```yaml
- text:clear | <name>
```
</details>

<details><summary><strong>integer</strong> — Modify an integer variable using an equation</summary>

```yaml
integer | <name> | <equation>
```
Example:
```yaml
- integer | <name> | <equation>
```
</details>

<details><summary><strong>table</strong> — Modify a table variable</summary>

```yaml
table | <name> | <entry> | <value>
```
Example:
```yaml
- table | <name> | <entry> | <value>
```
</details>

<details><summary><strong>list:append</strong> — Add an item to a list</summary>

```yaml
list:append | <name> | <text>
```
Example:
```yaml
- list:append | <name> | <text>
```
</details>

<details><summary><strong>list:prepend</strong> — Add an item to the start of a list</summary>

```yaml
list:prepend | <name> | <text>
```
Example:
```yaml
- list:prepend | <name> | <text>
```
</details>

<details><summary><strong>list:remove</strong> — Remove an item from a list</summary>

```yaml
list:remove | <name> | <text>
```
Example:
```yaml
- list:remove | <name> | <text>
```
</details>

<details><summary><strong>list:removeall</strong> — Remove all matching items from a list</summary>

```yaml
list:removeall | <name> | <text>
```
Example:
```yaml
- list:removeall | <name> | <text>
```
</details>

<details><summary><strong>list:clear</strong> — Clear all items from a list</summary>

```yaml
list:clear | <name>
```
Example:
```yaml
- list:clear | <name>
```
</details>

<details><summary><strong>boolean:true</strong> — Set a boolean to true</summary>

```yaml
boolean:true | <name>
```
Example:
```yaml
- boolean:true | <name>
```
</details>

<details><summary><strong>boolean:false</strong> — Set a boolean to false</summary>

```yaml
boolean:false | <name>
```
Example:
```yaml
- boolean:false | <name>
```
</details>

<details><summary><strong>boolean:toggle</strong> — Toggle a boolean value</summary>

```yaml
boolean:toggle | <name>
```
Example:
```yaml
- boolean:toggle | <name>
```
</details>

---

## ⚙️ **Utility**
<details><summary><strong>playsound</strong> — Play a sound file</summary>

```yaml
playsound | <sound_name>
```
Example:
```yaml
- playsound | <sound_name>
```
</details>

<details><summary><strong>wait</strong> — Pause execution</summary>

```yaml
wait | <seconds>
```
Example:
```yaml
- wait | <seconds>
```
</details>

<details><summary><strong>syscmd</strong> — Execute a system command</summary>

```yaml
syscmd | <command>
```
Example:
```yaml
- syscmd | <command>
```
</details>

<details><summary><strong>actionpack</strong> — Run a predefined action pack</summary>

```yaml
actionpack | <name>
```
Example:
```yaml
- actionpack | <name>
```
</details>

<details><summary><strong>notify</strong> — Display a notification</summary>

```yaml
notify | <text>
```
Example:
```yaml
- notify | <text>
```
</details>

---

## 🧠 **Advanced / System**
<details><summary><strong>conditional</strong> — Trigger a conditional</summary>

```yaml
conditional | <name>
```
Example:
```yaml
- conditional | <name>
```
**Learn more:** See the [Conditionals Reference](conditionals.md).
</details>

<details><summary><strong>webhook</strong> — Trigger a webhook</summary>

```yaml
webhook | <name>
```
Example:
```yaml
- webhook | <name>
```
</details>

<details><summary><strong>tts</strong> — Speak a message using Text-to-Speech</summary>

```yaml
tts | <voice> | <message> | [true/false] | [limit]
```
Example:
```yaml
- tts | <voice> | <message> | [true/false] | [limit]
```
</details>
