+++
title = "November 2020"
weight = 40
+++

# November 2020

Errors were modularized at the back of [Northstar](https://github.com/forgeflux-org/northstar/),
and A Docker CI was set up for the Northstar builds.

A [GitHub organization](https://github.com/forgeflux-org) was created for ForgeFedv2,
and the repositories for the projects were transferred over to it.

A Notification-Event Translation Mechanism was set up.

1. Northstar functionality was integrated into Interface, and tests were set up to ensure that it could be contacted through Interface's methods.
2. A locking mechanism was set up for concurrent operations on Git utilizing [Sled](https://sled.rs/).
3. Implementations of a basic job runner was set up to mimic retrieving requests from Forges, through periodically retrieving notifications.
4. The endpoints for notifications was subsequently set up, and responses to these Notifications were termed as [events](@/getting-started/events.md).
5. The endpoints for processing these events were then created.

Shifted over the configuration management to [Dynaconf](https://www.dynaconf.com/).

## References

-   Integration with Northstar :: [Info](https://github.com/forgeflux-org/interface/commit/0c9d8bdff05e668d77a85fdfc89b37abe1ac86cb)
-   Locking Mechanism with Sled :: [Info](https://github.com/forgeflux-org/interface/commit/d3e7c81c95d87b612ebb9562cac31d371fe8629e)
-   Defining Events :: [Info](https://github.com/forgeflux-org/interface/commit/30547b783578a7a9548aca55b3b7c932ed8130e6)
