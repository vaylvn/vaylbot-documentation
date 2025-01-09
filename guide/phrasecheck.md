# **PhraseCheck**

The **PhraseCheck** system in Vayl allows you to detect specific phrases in chat and trigger predefined actions. This feature is highly customizable and ensures dynamic interaction with your audience.

---

## **Phrase Structure**

Each phrase is defined in the `phrases.yml` file, located in the `configuration` folder. Below is the basic structure of a phrase definition:

```yaml
phrase:
    <phrase_string>:
        type: <type>
        cooldown: <time_in_seconds>
        actions:
        - <action>
```

### **Phrase Settings**
1. **`type`**:
   - Defines how the phrase is matched.
   - Options:
     - `"matches"`: Matches the exact phrase.
     - `"contains"`: Triggers when the phrase is contained anywhere in the chat message.

2. **`cooldown`**:
   - Prevents spam by setting the minimum time (in seconds) between repeated triggers for the same phrase.

3. **`actions`**:
   - A list of actions to trigger when the phrase is detected.
   - Actions support standard Vayl action tags (e.g., `[ruser]`, `[counter:name]`).

---

## **Example Configuration**

### **Detect an Exact Match**
The following example triggers an action when the exact message `^` is sent in chat:

```yaml
phrase:
    ^:
        type: matches
        cooldown: 0
        actions:
        - chat ; ^
```

- **Type**: Matches the exact `^` symbol.
- **Cooldown**: No cooldown (can trigger repeatedly).
- **Actions**: Sends `^` back into the chat.

### **Detect a Contained Phrase**
The following example triggers an action when the word "hello" appears anywhere in the chat message:

```yaml
phrase:
    hello:
        type: contains
        cooldown: 10
        actions:
        - chat ; Hello there, [user]!
```

- **Type**: Contains the word "hello."
- **Cooldown**: 10 seconds.
- **Actions**: Welcomes the user who typed "hello."

---

## **Best Practices**
1. **Avoid Overlapping Phrases**:
   - Ensure phrases do not conflict with each other to avoid unintended triggers.

2. **Set Appropriate Cooldowns**:
   - Use cooldowns to prevent spam and maintain smooth chat flow.

3. **Test Your Configuration**:
   - Verify your phrases and actions are working as intended before using them in a live stream.

---
