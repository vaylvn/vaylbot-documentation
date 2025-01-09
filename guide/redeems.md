# **Redeems**

Vayl Bot's **Redeems** functionality allows you to tie Twitch channel point redemptions to custom actions. This provides a flexible way to automate responses and actions when a viewer redeems a channel point reward.

---

## **Structure of `redeems.yml`**

The `redeems.yml` file is located within the `configuration` folder. Below is the structure of a typical redeem configuration:

```yaml
redeem:
  <redeem_name>:
    queue: <true_or_false>
    buffer: <time_in_seconds>
    actions:
    - <action>
```

### **Fields Explained**

1. **`<redeem_name>`**:
   - Acts as the identifier for the redeem.
   - This name must exactly match the name of the channel point redeem created on Twitch.

2. **`queue`**:
   - Determines whether the redeem alert is added to the front (`true`) or the back (`false`) of the alert queue.
   - **Example**:
     - Setting this to `true` prioritizes the redeem over others.

3. **`buffer`**:
   - Specifies how long Vayl should wait (in seconds) after this redeem is triggered before moving to the next alert.
   - Handy for spacing out consecutive alerts, especially if multiple actions are performed.

4. **`actions`**:
   - A list of actions to perform when the redeem is triggered.
   - Actions follow the same format as described in the [Actions Guide](actions.md).

---

## **Example Configuration**

Here’s an example configuration for a redeem called `testing`:

```yaml
redeem:
  testing:
    queue: true
    buffer: 5
    actions:
    - chat ; 'testing' redeem has been redeemed!
```

### **Explanation**
- **Redeem Name**: `testing`
  - This redeem is triggered when a Twitch channel point reward named `testing` is redeemed.
- **Queue**: `true`
  - This redeem will be added to the front of the alert queue.
- **Buffer**: `5`
  - Vayl will wait 5 seconds after processing this redeem before moving on to the next alert.
- **Actions**:
  - Sends a message in chat: `'testing' redeem has been redeemed!`

---

## **Usage Scenarios**

1. **Simple Chat Announcements**:
   - Announce in chat when a channel point redeem is used.
     ```yaml
     redeem:
       shoutout:
         queue: false
         buffer: 3
         actions:
         - chat ; '[user] redeemed a shoutout! Thank you!'
     ```

2. **Triggering OBS Effects**:
   - Tie channel point redeems to OBS actions like switching scenes or toggling sources.
     ```yaml
     redeem:
       spotlight:
         queue: true
         buffer: 10
         actions:
         - obs:toggle ; Spotlight Source
     ```

3. **Interactive Events**:
   - Combine multiple actions for engaging events.
     ```yaml
     redeem:
       fireworks:
         queue: true
         buffer: 15
         actions:
         - chat ; 'Get ready for fireworks!'
         - playsound ; fireworks
         - obs:toggle ; Fireworks Overlay
     ```

---

## **Best Practices**

1. **Match Names Exactly**:
   - Ensure the `redeem_name` in `redeems.yml` matches the Twitch channel point reward name exactly.

2. **Set Appropriate Buffers**:
   - Use `buffer` to prevent overlapping actions when multiple redeems are triggered consecutively.

3. **Leverage the Queue**:
   - Use `queue` to prioritize certain redeems when handling multiple alerts.

4. **Test Redeems**:
   - Test your redeems in a controlled environment to ensure they trigger as expected.
