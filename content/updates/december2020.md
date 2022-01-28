+++
title = "December 2020"
weight = 40
+++

# December 2020
## Northstar

As the development on [Northstar](@/services/northstar.md) nears the completion phase,
updates on it have slowed down, and the only updates that were made during this
stage mostly comprises of configuration updates.
These updates were mostly related to bootstrapping [DynaConf](https://www.dynaconf.com/), 
as we embraced 12-factor app configuration recommendations, allowing for better 
configuration management.

## Interface

Realising the need for validation of a request to an actor, an authentication 
mechanism was developed to implement Matrix's [signed JSON](https://github.com/matrix-org/python-signedjson)
feature, but, was later replaced in favor of [HTTP Signatures](https://tools.ietf.org/html/draft-cavage-http-signatures).

Interface underwent major refactoring to improve test-ability and reliability in addition 
to implementing authentication by a [signed JSON](https://github.com/matrix-org/python-signedjson)
mechanism implemented by the Matrix project. Taking note of rate-limits imposed by some forges, 
we figured we'd have to cache responses and so data persistence was implemented by way of 
storing in a database.

## References
These are a list of the Pull Requests where the following updates took place for the
organization.

- Forking Implementation :: [#34](https://github.com/forgeflux-org/interface/commit/5c9f61d60ce069963da7abc761b9ba3d81c8883a)
- Authentication :: [#36](https://github.com/forgeflux-org/interface/commit/5cc206cbe5be83cedac14949a537baad4c6351e3)
- DB Refactor :: [#39](https://github.com/forgeflux-org/interface/commit/57c9a085b38f8c3bab7975e18d21e4455ad3cac9), [#40](https://github.com/forgeflux-org/interface/commit/d9d785ca116e9a2bb9a40cf3eaa16a8b275d1593)
