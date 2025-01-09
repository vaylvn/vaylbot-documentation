# **Discord Webhooks**

Discord webhooks provide a powerful way to integrate Twitch stream events into a Discord server. By using Vayl’s webhook action, users can automate sending messages and embeds to their Discord channels, creating a more engaging experience for their community.

---

## **Webhook Configuration**

Webhooks are defined in individual YAML files located in your bot's configuration folder. Below is the structure of a webhook configuration:

```yaml
url: "<webhook_url>"
message:
- "<plain_text_message>"
embed:
  title: "<embed_title>"
  image-url: "<image_url>"
  thumbnail-url: "<thumbnail_url>"
  description:
  - "<embed_description>"
  fields:
    enabled: <true_or_false>
    1:
      name: "<field_1_name>"
      value: "<field_1_value>"
    2:
      name: "<field_2_name>"
      value: "<field_2_value>"
```

---

### **Fields Explained**

1. **`url`**:
   - The webhook URL obtained from Discord.
   - **How to Get It**:
     1. Go to your Discord server and navigate to **Server Settings > Integrations > Webhooks**.
     2. Create a new webhook and copy its URL.
     3. Paste the URL into the `url` field in your webhook file.

2. **`message`**:
   - Plain text messages that will appear in the Discord channel alongside the embed (optional).

3. **`embed`**:
   - Contains settings for the Discord embed:
     - **`title`**: The main title of the embed.
     - **`image-url`**: A large image displayed in the embed.
     - **`thumbnail-url`**: A smaller image displayed in the corner of the embed.
     - **`description`**: The main body text of the embed.
     - **`fields`**:
       - **`enabled`**: Whether custom fields are included in the embed (`true` or `false`).
       - **`1`, `2`, etc.**: Define custom fields with `name` and `value`.

---

## **Example Webhook**

Here’s an example of a webhook for announcing when the streamer is live:

```yaml
url: "https://discord.com/api/webhooks/1234567890/abcdefghijklmnopqrstuvwxyz"
message:
- "Hey! [name] is LIVE! Be sure to drop by and say hello!"
embed:
  title: "[name] is Streaming [game]!"
  image-url: "https://i.ibb.co/GvBKvK3/image.png"
  thumbnail-url: "https://i.ibb.co/5ctPXKT/thumbnail.png"
  description:
  - "Come join the fun and chat with [name] while they play [game]!"
  fields:
    enabled: true
    1:
      name: View Stream
      value: "[link]"
    2:
      name: Current Game
      value: "[game]"
```

---

## **Using Tags**

Webhooks support dynamic tags within their messages to personalize responses. These tags are replaced with relevant data when the webhook is sent:

1. **`[game]`**: The current game being streamed.
2. **`[title]`**: The current stream title.
3. **`[name]`**: The streamer’s Twitch username.
4. **`[link]`**: A direct link to the streamer’s Twitch channel.
5. **Other Standard Tags**: Tags like `[ruser]` or `[arg1]` can also be used if applicable.

---

## **Triggering Webhooks**

Webhooks are an action in Vayl and can be triggered from any action list. Examples include:
- Announcing stream start or end:
  ```yaml
  - webhook ; streamonline
  - webhook ; streamoffline
  ```
- Announcing raids:
  ```yaml
  - webhook ; raid
  ```
- Relaying Twitch chat to Discord:
  ```yaml
  - webhook ; chatlog
  ```

---

## **Best Practices**

1. **Test Webhooks**:
   - Before going live, ensure your webhook files are configured correctly and sending to the appropriate Discord channel.

2. **Use Tags Effectively**:
   - Incorporate dynamic tags to create personalized and engaging messages.

3. **Limit Frequency**:
   - Avoid overwhelming your Discord channel with excessive messages by setting reasonable triggers.

