# Actions Documentation

This document describes all available actions in **Vayl**, including their arguments, descriptions, and usage examples.

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
- **Description**: Toggles visibility of the specified source in OBS.
- **Arguments**:
  - `source_name` (string): The name of the source to toggle.
- **Usage**: `obs:toggle ; source_name`

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

---

## Variable Management

### `text`
- **Description**: Modifies a text variable.
- **Arguments**:
  - `name` (string): Name of the variable.
  - `action` (string): `set` or `append`.
  - `text` (string): Value to set or append.
- **Usage**: `text ; name ; action ; text`

---

## Advanced Actions

### `tts`
- **Description**: Generates a text-to-speech message.
- **Arguments**:
  - `voice` (string): Voice type.
  - `message` (string): TTS content.
  - `halt` (boolean): Whether to stop previous playback (`true`/`false`).
  - `char_limit` (integer): Maximum character length.
- **Usage**: `tts ; voice ; message ; halt ; char_limit`

### `cmd`
- **Description**: Executes a system command.
- **Arguments**:
  - `command` (string): Command to run.
- **Usage**: `cmd ; command`

---
