# Twitch Event Reference

Each supported event has a corresponding configuration file inside:

```
configuration/event/
```

These `.yml` files let you:
- Enable or disable the event (`enabled: true/false`)
- Define its queue behavior (`queue: front/back/instant`)
- Assign a list of actions to execute when triggered

Example configuration:
```yaml
enabled: true
queue: front
actions:
- chat | Hello, [user_name]!
```

### Queue Behavior
| Value | Description |
|--------|--------------|
| **front** | Places the event at the front of the queue, but still waits for any currently playing alert to finish. |
| **back** | Places the event at the back of the queue. |
| **instant** | Triggers immediately, bypassing the queue. |

All events expose a set of tags (e.g. `[user_name]`, `[broadcaster_user_name]`, `[title]`) that can be used inside your actions.

> **Note:** The **Redeem** (Reward Add) event has its own dedicated configuration page — see [redeems.md](redeems.md).

---

## Supported Events

<details><summary><strong>Ad Break Begin</strong> — Triggered when an ad break starts.</summary>

| Tag | Description |
|------|-------------|
| [duration_seconds] | Length of the ad break in seconds. |
| [started_at] | Time the ad break started. |
| [is_automatic] | Whether the ad break was automatically triggered. |
| [broadcaster_user_name] | Display name of the broadcaster. |
| [requester_user_name] | Name of the user who requested the ad break. |

</details>

<details><summary><strong>Cheer</strong> — Triggered when a user sends bits in chat.</summary>

| Tag | Description |
|------|-------------|
| [is_anonymous] | Whether the cheer was sent anonymously. |
| [user_name] | Display name of the cheering user. |
| [message] | Message attached to the cheer. |
| [bits] | Number of bits cheered. |
| [broadcaster_user_name] | Display name of the broadcaster. |

</details>

<details><summary><strong>Follow</strong> — Triggered when a user follows the broadcaster.</summary>

| Tag | Description |
|------|-------------|
| [user_name] | Display name of the follower. |
| [user_login] | Login name of the follower. |
| [followed_at] | Time the follow occurred. |
| [broadcaster_user_name] | Display name of the broadcaster. |

</details>

<details><summary><strong>Hype Train Begin</strong> — Triggered when a new Hype Train starts.</summary>

| Tag | Description |
|------|-------------|
| [id] | ID of the hype train. |
| [total] | Total contributions to the hype train. |
| [progress] | Current progress value. |
| [goal] | Required value to complete the level. |
| [level] | Current hype train level. |
| [top_contributions.1.user_name] | Name of a top contributor. |
| [top_contributions.1.total] | Total contribution from the user. |
| [started_at] | Start time of the hype train. |
| [expires_at] | When the hype train ends. |

</details>

<details><summary><strong>Poll Begin</strong> — Triggered when a new poll starts.</summary>

| Tag | Description |
|------|-------------|
| [id] | Poll ID. |
| [title] | Title of the poll. |
| [choices.1.title] | Title of a poll choice. |
| [bits_voting.is_enabled] | Whether bit voting is enabled. |
| [channel_points_voting.is_enabled] | Whether channel points voting is enabled. |
| [started_at] | Time the poll began. |
| [ends_at] | When the poll will end. |

</details>

<details><summary><strong>Poll End</strong> — Triggered when a poll ends.</summary>

| Tag | Description |
|------|-------------|
| [id] | Poll ID. |
| [title] | Title of the poll. |
| [choices.1.title] | Title of a poll choice. |
| [choices.1.votes] | Total votes for that choice. |
| [status] | Final poll status (e.g., completed). |
| [ended_at] | Time the poll ended. |

</details>

<details><summary><strong>Prediction Begin</strong> — Triggered when a new prediction starts.</summary>

| Tag | Description |
|------|-------------|
| [id] | Prediction ID. |
| [title] | Title of the prediction. |
| [outcomes.1.title] | Title of a prediction outcome. |
| [outcomes.1.color] | Color assigned to the outcome. |
| [started_at] | Start time of the prediction. |
| [locks_at] | When the prediction locks. |

</details>

<details><summary><strong>Prediction Lock</strong> — Triggered when predictions lock.</summary>

| Tag | Description |
|------|-------------|
| [id] | Prediction ID. |
| [title] | Prediction title. |
| [outcomes.1.title] | Outcome title. |
| [outcomes.1.users] | Number of users who voted. |
| [outcomes.1.channel_points] | Total points used for this outcome. |
| [outcomes.1.top_predictors.1.user_name] | Name of a top predictor. |
| [locked_at] | Time the prediction was locked. |

</details>

<details><summary><strong>Prediction End</strong> — Triggered when a prediction resolves.</summary>

| Tag | Description |
|------|-------------|
| [id] | Prediction ID. |
| [title] | Prediction title. |
| [winning_outcome_id] | ID of the winning outcome. |
| [outcomes.1.title] | Outcome title. |
| [outcomes.1.users] | Number of users who voted for that outcome. |
| [outcomes.1.channel_points] | Total channel points wagered. |
| [status] | Final prediction status (resolved/canceled). |
| [ended_at] | When the prediction ended. |

</details>

<details><summary><strong>Redeem</strong> — Triggered when a custom channel point reward is redeemed.</summary>

See [redeems.md](redeems.md) for full configuration and tag details.

</details>

<details><summary><strong>Redeem Update</strong> — Triggered when a custom reward redemption is updated (fulfilled or canceled).</summary>

| Tag | Description |
|------|-------------|
| [id] | Redemption ID. |
| [user_name] | Name of the user who redeemed the reward. |
| [user_input] | Text input submitted with the redemption. |
| [status] | Redemption status (fulfilled/canceled). |
| [reward.title] | Title of the redeemed reward. |
| [redeemed_at] | Time the redemption was created. |

</details>

<details><summary><strong>Subscription</strong> — Triggered when a new user subscribes.</summary>

| Tag | Description |
|------|-------------|
| [user_name] | Name of the subscribing user. |
| [tier] | Subscription tier (e.g., 1000, 2000, 3000). |
| [is_gift] | Whether the sub was a gift. |

</details>

<details><summary><strong>Subscription – ReSub</strong> — Triggered when a returning subscriber shares their renewal message.</summary>

| Tag | Description |
|------|-------------|
| [user_name] | Name of the resubscribing user. |
| [message.text] | Text of the user’s resub message. |
| [message.emotes.1.id] | ID of an emote in the message. |
| [cumulative_months] | Total months subscribed. |
| [streak_months] | Current streak length (if shared). |
| [duration_months] | Months purchased in this sub. |

</details>

<details><summary><strong>Subscription – GiftSub</strong> — Triggered when a user gifts one or more subs.</summary>

| Tag | Description |
|------|-------------|
| [user_name] | Name of the gifter. |
| [total] | Number of subs gifted in this event. |
| [tier] | Tier of the gifted subscription. |
| [cumulative_total] | Total subs gifted by this user (if shared). |
| [is_anonymous] | Whether the gift was anonymous. |

</details>

<details><summary><strong>Shoutout Create</strong> — Triggered when the broadcaster gives a shoutout to another channel.</summary>

| Tag | Description |
|------|-------------|
| [broadcaster_user_name] | Name of the sending broadcaster. |
| [to_broadcaster_user_name] | Name of the receiving broadcaster. |
| [viewer_count] | Viewers during the shoutout. |
| [started_at] | When the shoutout began. |
| [cooldown_ends_at] | When the cooldown ends for the broadcaster. |
| [target_cooldown_ends_at] | When the cooldown ends for the target. |

</details>

<details><summary><strong>Shoutout Receive</strong> — Triggered when the broadcaster receives a shoutout.</summary>

| Tag | Description |
|------|-------------|
| [broadcaster_user_name] | Name of the receiving broadcaster. |
| [from_broadcaster_user_name] | Name of the sending broadcaster. |
| [viewer_count] | Viewer count during the shoutout. |
| [started_at] | Time the shoutout began. |

</details>

<details><summary><strong>Stream Offline</strong> — Triggered when the stream goes offline.</summary>

| Tag | Description |
|------|-------------|
| [broadcaster_user_name] | Display name of the broadcaster. |

</details>

<details><summary><strong>Stream Online</strong> — Triggered when the stream goes live.</summary>

| Tag | Description |
|------|-------------|
| [id] | Stream ID. |
| [broadcaster_user_name] | Display name of the broadcaster. |
| [type] | Stream type (e.g., live). |
| [started_at] | Time the stream started. |

</details>
