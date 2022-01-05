+++
title = "Services"
weight = 15
+++

# Services
The services that are currently in active development are Northstar, and Interface.
However, here's a few more details about them.

## Northstar
- Repository :: [Source Code](https://github.com/forgeflux-org/northstar)
- OpenAPI :: [OpenAPI Specification](https://northstar.forgeflux.org/docs/openapi/)

ForgeFlux allows for multiple interfaces to be run against a single software forge.
Also, the protocol is flexible enough to support multiple types of software forges(GitLab, GitHub, etc).
The protocol's decentralised nature makes it impossible to create a constant record of which interfaces service forges.

So we created a discovery service which stores records of interfaces and the forges they service.
This is very similar to the way DNS works.
In DNS, hostname is resolved to IP address.

Here, software forge URL is resolved to URLs of [interfaces](https://github.com/forgeflux-org/interface) that service the queried forge.

For an extensive view on Northstar, please check [Northstar::Detailed](@/services/northstar.md)

## Interface
- Repository :: [Source Code](https://github.com/forgeflux-org/interface)
- OpenAPI :: [OpenAPI Specification](https://github.com/forgeflux-org/interface/tree/master/docs/openapi)

Developing Free Software is about liberating users and giving them total control over how the programs they run should work.
It's only fair that developers of such software enjoy the same levels of liberty.

ForgeFlux is an attempt to enable federation for major software forges (GitLab, GitHub, Gitea, Source Hut, etc) entirely in API-space.
We believe our API-space implementation will allow for more organic growth as it will not require any involvement from the forge developers.

