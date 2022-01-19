+++
title = "How does it work?"
weight = 40
+++

# How does it work?

Bridges connect people, and so does ForgeFlux!

Similar to how bridges are made, with two connecting endpoints for the start point and the end point, ForgeFlux does the same with Interfaces.

[Interfaces](@/services/interface.md) are services that are run on the side of any user, and are used as connecting points of the bridge.
These interfaces are responsible for communicating with each other, and interact in the form of messages for a server-server model, and a REST API model for the server-user model.

Interfaces are geared towards performing various operations for the repository, which include but are not limited to,

-   Pull Requests
-   Issues
-   Comments
-   Notifications
-   Forking

Recently, ForgeFlux has moved towards implementing the [ActivityPub protocol](https://activitypub.rocks/) for interoperability with various Social Networking implementations as well. \
Implementing the ActivityPub protocol, we've currently established three Actors in the environment, Repositories, Issues/Pull Requests, and Users.
This way, you can only subscribe to actors and if someone is interested in only a single issue, they would only be required to interact with that particular Actor rather than
the entire repository.

Deviating from the method that ForgeFed follows, Git is used for changes in the Git repository. \
While [ForgeFed Section 5.2](https://forgefed.peers.community/behavior.html#push-activity) mandates a Push activity to be sent out to all followers whenever there's a `git push`,
it is not feasible for external implementations like ForgeFlux, which leverage the Forge APIs, to perform this operation since we'll have to consider the API rate limits.

Here, we are deviating again from ForgeFed by making it optional.
So, federating forges/interfaces will have to periodically do a `git pull` to receive changes.

For operations such as Issues and Pull Requests, we utilize ActivityPub.
This is quite similar to [how Mastodon works](https://docs.joinmastodon.org/spec/activitypub/).

However, as the count for interfaces go up in magnitudes, it becomes increasingly hard to keep track of them.
This is where [Northstar](@/services/northstar.md) comes to play, by implementing a lookup server that seeks to provide an indexed list of available forge interfaces.

ForgeFlux is currently in the Active Development phase, and is being worked on towards the alpha-testing stage.
