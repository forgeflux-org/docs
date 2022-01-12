+++
title = "How does it work?"
weight = 40
+++

# How does it work?
Interfaces are services that are run on the side of any user, and are used as connecting points of the bridge.
These interfaces are responsible for communicating with each other, and interact in the form of messages for a server-server model, and a REST API model for the server-user model.

Interfaces are geared towards performing various operations for the repository, which include but are not limited to,
- Pull Requests
- Issues
- Comments
- Notifications
- Forking

However, as the count for interfaces go up in magnitudes, it becomes increasingly hard to keep track of them.
This is where Northstar comes to play, by implementing a lookup server that seeks to provide an indexed list of available forge interfaces.

ForgeFlux is currently in the Active Development phase, and is being worked on towards the alpha-testing stage.

