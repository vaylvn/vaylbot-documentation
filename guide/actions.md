# Actions

This document describes all available actions in **Vayl**, including their arguments, descriptions, and usage examples.
For a list of available [tags], [click here.](https://github.com/vaylvn/vaylbot-documentation/blob/main/guide/conditional-actions.md#tags-for-fetching-information)

---

## OBS Integrations

### `obs:scene`
- **Description**: Sets the current scene in OBS.
- **Arguments**:
  - `scene_name` (string): The name of the scene.
- **Usage**: `obs:scene ; scene_name`

### `obs:show`
- **Description**: Shows the specified source in OBS.
- **Arguments**:
  - `source_name` (string): The name of the source to show.
- **Usage**: `obs:show ; source_name`

### `obs:hide`
- **Description**: Hides the specified source in OBS.
- **Arguments**:
  - `source_name` (string): The name of the source to hide.
- **Usage**: `obs:hide ; source_name`

### `obs:toggle`
- **Description**: Toggles the visibility of the specified source in OBS.
- **Arguments**:
  - `source_name` (string): The name of the source to toggle.
- **Usage**: `obs:toggle ; source_name`

### `obs:label`
- **Description**: Sets the contents of the specified label in OBS.
- **Arguments**:
  - `source_name` (string): The name of the label source.
  - `text` (string): The new text for the label.
  - `color` (string): Text color (e.g., `#FFFFFF` for white).
- **Usage**: `obs:label ; source_name ; text ; color`

### `obs:mediafile`
- **Description**: Sets the filepath for a media source in OBS.
- **Arguments**:
  - `source_name` (string): The name of the media source.
  - `filepath` (string): Path to the media file.
- **Usage**: `obs:mediafile ; source_name ; filepath`

### `obs:slideshow`
- **Description**: Controls a slideshow source in OBS.
- **Arguments**:
  - `source_name` (string): The name of the slideshow source.
  - `action` (string): One of `play`, `pause`, `stop`, `restart`, `next`, `previous`, or `position`.
- **Usage**: `obs:slideshow ; source_name ; action`

### `obs:filter`
- **Description**: Enables or disables a filter on an OBS source.
- **Arguments**:
  - `filter_name` (string): The filter name.
  - `enabled` (boolean): `true` to enable, `false` to disable.
- **Usage**: `obs:filter ; filter_name ; enabled`

---

## General Actions

### `playsound`
- **Description**: Plays a sound file from the sound directory.
- **Arguments**:
  - `file_name` (string): Name of the sound file.
- **Usage**: `playsound ; file_name`

### `wait`
- **Description**: Waits for a specified time before the next action.
- **Arguments**:
  - `time` (float): Time in seconds.
- **Usage**: `wait ; time`

### `console`
- **Description**: Prints a message to the Vayl console.
- **Arguments**:
  - `message` (string): The content to print.
- **Usage**: `console ; message`

### `cmd`
- **Description**: Executes a command via Command Prompt.
- **Arguments**:
  - `command` (string): Command to run.
- **Usage**: `cmd ; command`

---

## Advanced Actions

### `tts`
- **Description**: Generates a text-to-speech message.
- **Arguments**:
  - `voice` (string): Voice type.
  - `message` (string): TTS content.
  - `halt` (boolean): Whether to halt subsequent actions. (`true`/`false`).
  - `char_limit` (integer): Maximum character length.
- **Usage**: `tts ; voice ; message ; halt ; char_limit`

### `conditional`
- **Description**: Triggers a conditional (or nested) action defined in `configuration/conditionals`.
- **Arguments**:
  - `name` (string): Name of the conditional action.
- **Usage**:
  - `conditional ; name` (triggers the "name" conditional in 'configuration/conditionals')
  - `conditional ; name:subname` (triggers the "subname" conditional in 'configuration/conditionals/name.yml')

### `webhook`
- **Description**: Triggers a webhook defined in `configuration/webhook`.
- **Arguments**:
  - `name` (string): Name of the webhook.
- **Usage**: `webhook ; name`

---

## Chat Management

### `chat`
- **Description**: Sends a message in the streamer’s chat.
- **Arguments**:
  - `message` (string): The message to send.
- **Usage**: `chat ; message`

### `announce`
- **Description**: Sends an announcement message in chat.
- **Arguments**:
  - `message` (string): The announcement to send.
  - `color` (string): The color to use `("blue", "green", "orange", "purple", "primary")`
- **Usage**: `announce ; message ; color`

### `vip`
- **Description**: Adds or removes a user as a VIP.
- **Arguments**:
  - `action` (string): `add` or `remove`.
  - `user` (string): Username to modify.
- **Usage**: `vip ; action ; user`

### `timeout`
- **Description**: Places a user in timeout for a given duration with reaosn.
- **Arguments**:
  - `user` (string): Name of the user.
  - `duration` (int): Duration of the timeout.
  - `reason` (string): Reason for the timeout.
- **Usage**: `timeout ; user ; duration ; reason`

---

## Variables

### `text`
- **Description**: Modifies a text variable.
- **Arguments**:
  - `name` (string): Name of the variable.
  - `action` (string): `set` or `append`.
  - `text` (string): Value to set or append.
- **Usage**: `text ; name ; action ; text`

### `counter`
- **Description**: Modifies a counter variable.
- **Arguments**:
  - `name` (string): Counter name.
  - `action` (string): `set`, `increase`, `decrease`, `multiply` or `divide`.
  - `amount` (integer): Value to adjust by.
- **Usage**: `counter ; name ; action ; amount`

### `boolean`
- **Description**: Modifies a boolean variable.
- **Arguments**:
  - `name` (string): Name of the variable.
  - `action` (string): `true`, `false`, or `toggle`.
- **Usage**: `boolean ; name ; action`

### `list`
- **Description**: Modifies a list variable.
- **Arguments**:
  - `name` (string): Name of the list variable.
  - `action` (string): `add`, `remove`, or `clear`.
  - `text` (string): Item to add or remove.
- **Usage**: `list ; name ; action ; text`

---

## Timed Actions

Timed actions allow users to trigger a set of actions at regular intervals. These are defined in the `timed-actions.yml` file located in the `configuration` folder.

### **Structure of a Timed Action**

```yaml
actions:
  <unique_name>:
    max-iterations: <number>
    frequency: <time_in_seconds>
    actions:
    - <action>
```

### **Fields Explained**

1. **`<unique_name>`**:
   - A unique identifier for the timed action.

2. **`max-iterations`**:
   - The maximum number of times the timed action will trigger.
   - Set to `9999` for near-unlimited iterations.

3. **`frequency`**:
   - The time interval (in seconds) between each trigger.

4. **`actions`**:
   - A list of actions to execute at each interval.

### **Example Timed Action**

Here’s an example of a timed action that periodically thanks the chat for watching:

```yaml
actions:
  thanks:
    max-iterations: 9999
    frequency: 1800
    actions:
    - chat ; Thanks for checking out the channel!
```

### **Usage Scenarios**

1. **Engagement Messages**:
   - Periodically thank viewers or encourage engagement.

2. **Promotional Reminders**:
   - Prompt viewers to visit your socials, join your Discord, or follow the channel.

3. **Creative Uses**:
   - Announce random questions or fun facts to spark interaction in chat.

---
