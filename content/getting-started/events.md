+++
title = "Events"
weight = 40
+++

# Events

Events are those operations that are performed on the Forge side,
such as Pull Requests, and Issues.

These events are operations of their own, and are handled within Interface
through Notifications.

The flow of processing an operation in the forge is done as follows,

1. We poll for Notifications through the [Job Runner](https://github.com/forgeflux-org/interface/blob/master/interface/runner/runner.py).
2. Proceed to send over this Notification to the Events Endpoint, where the Notification is parsed, and processed.
3. After identification, it is converted into a event, PR or Issue.

## References

-   Events Endpoint :: [Info](https://github.com/forgeflux-org/interface/blob/master/interface/runner/events.py)
