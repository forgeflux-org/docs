+++
title = "Interface"
weight = 40
+++

# Interface

Interface is a service that acts as a connecting end of the bridge, listening
in for Notifications from a particular forge repository.

These notifications, which may be in the form of a Comment, Issue, or Pull Request,
are then further defined into [Events](@/getting-started/events.md) to create
a workable unit set, that the interface can use to translate operations from
one forge to another forge.

The procedure of the Notification-Event Translation System, works as follows,

1. Upon creation of the Interface, and set up of a forge repository to look for, the interface subscribes to the forge's notifications.
2. Every notification received by the interface from the forges, is then identified and translated into it's respective `Event` model, be it an Issue or PR.
3. Upon conversion into the respective model, Interface processes these `Events`, and converts them into the model required for the destination forge.
