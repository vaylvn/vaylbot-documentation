# **Default Commands**
Looking for [Custom Commands?](custom-commands.md)

Vayl Bot includes a set of default commands to simplify stream management and enhance viewer interaction. Below is a comprehensive list of the commands, categorized by their access levels and functionality.

---

## **Streamer and Moderator Commands**

### `!setgame`

- **Access**: Streamer and Moderators
- **Description**: Updates the stream's current game.
- **Example**:
  ```
  !setgame Minecraft
  ```

### `!settitle`

- **Access**: Streamer and Moderators
- **Description**: Updates the stream's title.
- **Example**:
  ```
  !settitle Building an Epic Base!
  ```

### `!addquote`

- **Access**: Streamer and Moderators
- **Description**: Saves a chat message as a quote. Must be used as a reply to the message.

---

## **Streamer-Only Commands**

# Vayl Bot Commands

## Debug Command

The `!debug` command allows users to simulate various bot events for testing purposes. Some event types take no arguments, while others can be customized using specific arguments and their shorthand prefixes.

### Usage

```plaintext
!debug <event_type> [arguments]
```

### Event Types Without Arguments
These event types are called simply by typing `!debug` followed by the event type:

- `ad-break`
- `vayl-load`
- `stream-online`
- `stream-offline`

### Event Types With Arguments
These event types allow customization through specific arguments:

- **`sub`**:
  - **Available Arguments**: `user` (`u`), `tier` (`t`), `months` (`m`), `message` (`msg`)

- **`giftsub`**:
  - **Available Arguments**: `user` (`u`), `tier` (`t`), `gifts` (`g`)

- **`hypetrain`**:
  - **Available Arguments**: `level` (`l`)

- **`first-time-chat`**, **`first-session-chat`**, **`follow`**:
  - **Available Arguments**: `user` (`u`)

- **`raid`**, **`shoutout-give`**, **`shoutout-receive`**:
  - **Available Arguments**: `user` (`u`), `viewers` (`v`)

- **`bits`**:
  - **Available Arguments**: `user` (`u`), `amount` (`b`), `message` (`msg`)

### Argument Prefixes

To customize arguments for event types, use the prefixes (or their shorthand versions) as follows:

- `user:` or `u:`
- `tier:` or `t:`
- `months:` or `m:`
- `gifts:` or `g:`
- `message:` or `msg:`
- `bits:` or `b:`
- `level:` or `l:`
- `viewers:` or `v:`

### Examples

To simulate a subscription with a specific user and tier:

```plaintext
!debug sub u:TestUser t:2
```

To simulate a raid with a custom viewer count:

```plaintext
!debug raid u:RaiderUser v:50
```


### `!reload`

- **Access**: Streamer Only
- **Description**: Reloads Vayl to apply updated configurations.

---

## **Commands for All Users**

### `!game`

- **Access**: All Users
- **Description**: Displays the current game being streamed.

### `!uptime`

- **Access**: All Users
- **Description**: Displays the current stream uptime.

### `!quotes`

- **Access**: All Users
- **Description**: Displays the total number of quotes saved.

### `!quote <number>`

- **Access**: All Users
- **Description**: Displays the specified quote by its number.
- **Example**:
  ```
  !quote 5
  ```

### `!followage <user>`

- **Access**: All Users
- **Description**: Displays how long the specified user has been following the channel.
- **Example**:
  ```
  !followage SomeViewer
  ```

---
