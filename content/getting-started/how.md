+++
title = "How does it work?"
weight = 40
+++

# How does it work?

Bridges connect people, and so does ForgeFlux!

## Interface

The bridging component in ForgeFlux is called Interface.

[Interfaces](@/services/interface.md) are programs that run on either
side of the bridge, i.e, a bridge requires the participation of two
interfaces. Currently, Interfaces bridge the following operations:

-   Pull Requests
-   Issues
-   Comments

An Interface implementation for a software forge is able to
talk to the forge's API and speak [ActivityPub
protocol](https://activitypub.rocks/) for server-to-server
communications. This architecture makes it possible to implement an
Interface for any forge setup.

## Northstar

Since Interfaces run external to the forges, a method to find Interfaces
that service forges was required.

[Northstar](@/services/northstar.md) is a discovery service that maps an
Interface and the forge that it services. It acts very similar to DNS,
except instead of querying host names with intent to find corresponding
IP address, Northstar is queried with the forge's host name to discover
the Interfaces that service it.

## Resources

-
  [ecosystem-architecture](https://github.com/forgeflux-org/spec/blob/master/rfc/1-ecosystem-architecture/1-ecosystem-architecture.md):
  describes basic architecture and terminology used in ForgeFlux
