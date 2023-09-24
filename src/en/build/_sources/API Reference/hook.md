# Linking functions
With misspy, the functions that are called when using Streaming must be linked in advance using a system called hooks.

The hook system can also be used for functions that are essentially in separate files (the main bot is in a.py, the calling function is in b.py, etc.).
## How to Use
If you want to add a hook, you can do it with `hook.add(event name, function at event)`.

If you want to remove a hook, you can execute it with `hook.remove(event name)`.

If you want to **reload** the hook, you can do it with `hook.reload(event name)`.

## event list
| Event name | When called |
| ---------- | ----------------------- ------------ |
| note | Notes (including Renote) received |
| follow | Followed? |
| followed | Did you follow? |
| unfollow | Unfollowed? |
| mention | Mentioned? |
| ready | Connected to WebSocket |
| reply | Reply? |
| renote | Renote? |
| reacted | A reaction was added to the captured note |
| unreacted | The reaction of the captured note has been canceled |
| pollVoted | The note you are capturing was voted |
| deleted | The captured note has been deleted |