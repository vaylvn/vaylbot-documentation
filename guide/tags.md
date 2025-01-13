## Tags for Fetching Information

The following tags can be used within a condition to dynamically fetch information:

### General Tags
- `[system:dateus]`: Returns the current date in US format (MM/DD/YYYY).
- `[system:dateuk]`: Returns the current date in UK format (DD/MM/YYYY).
- `[system:time]`: Returns the current time in HH:MM:SS format.
- `[uptime:seconds]`: Returns the total stream uptime in seconds.
- `[viewers]`: Returns the stream's current viewercount.
- `[ruser]`: Returns a random user from the chat.
- `[followers]`: Returns the total follower count.
- `[subscribers]`: Returns the total subscriber count.
- `[ugame:user]`: Returns the current stream game for the specified `user`.

### Variables
- `[counter:name]`: Returns the value of the counter file called `name`.
- `[text:name]`: Returns the value of the text file called `name`.
- `[boolean:name]`: Returns the value of the boolean file called `name`.
- `[list:name]`: Returns the value of the list file called `name`.

### Randomization
- `[rfollower]`: Returns a random follower's username.
- `[rsubscriber]`: Returns a random subscribers's username.
- `[rnumber:min-max]`: Returns a random number within the given range.
- `[rlist:name]`: Returns a random item from the specified list.

### String Manipulation
- `[xstring:text:amount]`: Returns the given `text` repeated `amount` times.
- `[nickname:user]`: Returns the `nickname` (configuration/nicknames.yml) of the given `user`.
