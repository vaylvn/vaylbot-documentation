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

<details>
<summary><strong>obs:scene</strong> — Switch to a specific OBS scene</summary>

**Syntax:**
```yaml
obs:scene | <scene_name>
```

**Example:**
```yaml
- obs:scene | Starting Soon
```

| Argument | Description |
|-----------|-------------|
| **scene_name** | The exact name of the OBS scene. |

</details>

---

<details>
<summary><strong>obs:show</strong> — Show a specific OBS source</summary>

**Syntax:**
```yaml
obs:show | <source>
```

**Example:**
```yaml
- obs:show | Webcam
```

| Argument | Description |
|-----------|-------------|
| **source** | Source name in OBS. |

</details>

---

<details>
<summary><strong>obs:label</strong> — Update the text or color of a label source</summary>

**Syntax:**
```yaml
obs:label | <source> | <text> | [color]
```

**Example:**
```yaml
- obs:label | StreamTitle | [counter:subs] Subs | #FFFFFF
```

| Argument | Description |
|-----------|-------------|
| **source** | Label source name in OBS. |
| **text** | Text content to display. |
| **color** | Optional hex color (e.g. `#FFFFFF`). |

</details>

---

## 💬 **Chat & Messaging**

<details>
<summary><strong>chat</strong> — Send a message in chat</summary>

**Syntax:**
```yaml
chat | <message>
```

**Example:**
```yaml
- chat | Hello [user]!
```

| Argument | Description |
|-----------|-------------|
| **message** | Message to send. Supports tags. |

</details>

---

<details>
<summary><strong>announce</strong> — Send an announcement message</summary>

**Syntax:**
```yaml
announce | <message>
```

**Example:**
```yaml
- announce | Stream starting soon!
```

| Argument | Description |
|-----------|-------------|
| **message** | Text for the announcement. |

</details>

---

## 🔢 **Variables**

<details>
<summary><strong>counter</strong> — Modify a numeric counter variable</summary>

**Syntax:**
```yaml
counter | <name> | <action> | [amount]
```

**Example:**
```yaml
- counter | deaths | increase | 1
```

| Argument | Description |
|-----------|-------------|
| **name** | Counter variable name. |
| **action** | One of `set`, `increase`, `decrease`, `multiply`, `divide`. |
| **amount** | Optional numeric value to apply. |

</details>

---

<details>
<summary><strong>list</strong> — Modify list variables</summary>

**Syntax:**
```yaml
list | <name> | <action> | [text]
```

**Example:**
```yaml
- list | viewers | add | [user]
```

| Argument | Description |
|-----------|-------------|
| **name** | List variable name. |
| **action** | One of `add`, `remove`, `clear`. |
| **text** | Optional item text for add/remove. |

</details>

---

<details>
<summary><strong>text</strong> — Modify text variables</summary>

**Syntax:**
```yaml
text | <name> | <action> | <text>
```

**Example:**
```yaml
- text | status | set | Stream is live!
```

| Argument | Description |
|-----------|-------------|
| **name** | Variable name. |
| **action** | One of `set` or `append`. |
| **text** | The text content to use. |

</details>

---

## ⚙️ **Utility**

<details>
<summary><strong>sound</strong> — Play a sound file</summary>

**Syntax:**
```yaml
sound | <file_name>
```

**Example:**
```yaml
- sound | ding.wav
```

| Argument | Description |
|-----------|-------------|
| **file_name** | The sound file name (must exist in the `sounds` folder). |

</details>

---

<details>
<summary><strong>wait</strong> — Pause execution for a set number of seconds</summary>

**Syntax:**
```yaml
wait | <seconds>
```

**Example:**
```yaml
- wait | 5
```

| Argument | Description |
|-----------|-------------|
| **seconds** | Time to wait (can be decimal). |

</details>

---

<details>
<summary><strong>console</strong> — Print a message to the Vayl console</summary>

**Syntax:**
```yaml
console | <message>
```

**Example:**
```yaml
- console | Action triggered successfully
```

| Argument | Description |
|-----------|-------------|
| **message** | Text to print to the console. |

</details>

---

## 🧠 **Advanced / System**

<details>
<summary><strong>conditional</strong> — Trigger a conditional from configuration</summary>

**Syntax:**
```yaml
conditional | <name>
```

**Example:**
```yaml
- conditional | hype_start
```

| Argument | Description |
|-----------|-------------|
| **name** | Conditional name or `name:subname`. |

</details>

---

<details>
<summary><strong>webhook</strong> — Trigger a configured webhook</summary>

**Syntax:**
```yaml
webhook | <name>
```

**Example:**
```yaml
- webhook | discord_notify
```

| Argument | Description |
|-----------|-------------|
| **name** | Webhook name (defined in `configuration/webhook`). |

</details>

---

<details>
<summary><strong>tts</strong> — Speak a message aloud via Text-to-Speech</summary>

**Syntax:**
```yaml
tts | <voice> | <message> | [halt] | [char_limit]
```

**Example:**
```yaml
- tts | Ivy | [user_input] | true | 500
```

| Argument | Description |
|-----------|-------------|
| **voice** | Voice name (e.g. `Ivy`, `Brian`). |
| **message** | Message text to speak. |
| **halt** | Optional boolean — wait for speech before continuing. |
| **char_limit** | Optional integer — skip if message exceeds this length. |

</details>

---
