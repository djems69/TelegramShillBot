### v0.9
##### 10/4/2021
- added `increase_wait_interval` as a config option, allowing users to gradually increase how frequent messages are sent to a channel
  - example:
  ```yaml
  ...
  # this example will send a message once every 10 minutues (600 seconds)
  # after every iteration, 1 minute (60 seconds) will be added to the previous attempt's wait interval
  # so here is an example sequence of operations:
  #   - 10m wait, send message, 10m + 1m = 11m
  #   - 11m wait, send message, 11m + 1m = 12m
  #   - 12m wait, send message, 12m + 1m = 13m
  #   - etc, etc, etc
  somerandomchannelname:
    message_type: short
    wait_interval: 600
    increase_wait_interval: 60
  ...
  ```

### v0.8
##### 10/1/2021
- improved Telethon error handling

### v0.7
##### 9/30/2021
- refactored `channel` implementation

### v0.6
##### 9/28/2021
- refactored `splay` implementation

### v0.5
##### 9/27/2021
- added `splay` to connection and message calls to avoid `FloodWaitError` errors

### v0.4
##### 9/24/2021
- added Telethon entity caching to avoid `FloodWaitError` errors

### v0.3
##### 9/23/2021
- added random `thank you`s to end of message to avoid getting banned

### v0.2
##### 9/9/2021
- added try/catch around `FloodWaitError` errors

### v0.1
- Hello, World!