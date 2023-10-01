+++
title = "Welcome to ForgeFlux Documentation"
insert_anchor_links = "right"
+++

## Status

This site is Work-in-Progress, and as such, everything is in an
incomplete-state.

## Source code

Split between two forges, slowly migrating to self-hosted
[Forgejo](https://forgejo.org) instance at
[git.batsense.net](https://git.batsense.net)

1. [git.batsense.net](https://git.batsense.net/ForgeFlux)
1. [GitHub](https://github.com/forgeflux-org)

## Projects Overview

### Project Status: what does it mean?

1. WIP: Code isn't usable.
2. Usable: Code works, but user experience isn't polished. Can be used
   with a bit of patience ;)
3. Production: Ready for use

### 1. Interface

-   [Source code](https://github.com/forgeflux-org/interface)
-   Status: WIP
-   Description: API-space software forge federation implementation.

Federation will take time to implement in most, popular software forge
implementations. Interface aims to use the forge's REST API or similar
and create a federation layer on top of it.

Currently, implementation has minimal support for Forgejo and Gitea. A
Forgejo user can be exposed to Fediverse through WebFinger using
Interface.

### 2. Northstar

-   [Source code](https://github.com/forgeflux-org/northstar)
-   Status: Production
-   Description: A lookup service for federating software forges
-   Flagship instance: [northstar.forgeflux.org](https://northstar.forgeflux.org)

Interface's API-based, external, third-party approach introduces a
unique problem: how to locate the internet address (hostname) of the
Interface that services a forgege? Enter Northstar. It is a simple
Key-Value search server that maps forges and internfaces

### 3. Starchart

-   [Source code](https://github.com/forgeflux-org/starchart)
-   Status: Usable
-   Description: Spider and search engine for federating forges
-   Flagship instance:
    [starchart.forgeflux.org](https://starchart.forgeflux.org)

Projects on centralized forges like GitHub and GitLab enjoy good
visibility through network effect, good search engine indexing and
through third-party tools like
[awesomeopensource.com/](https://awesomeopensource.com/).

Starchart aims to provide high-visibility for projects on independently
hosted forges by indexing them and exposing the index with a searchable
index. The index is designed to be replicated, so that new Starchart
instances can be bootstrapped from an existing Starchart instance's
data.

### 4. f3-rs

-   [Source code](https://git.batsense.net/ForgeFlux/f3-rs)
-   Status: WIP
-   Description: Rust port of the [Friendly Forge Format](https://f3.forgefriends.org/) library
-   Documentation link: [f3.forgeflux.org](https://forgeflux.org)

### 4. ftest

-   [Source code](https://git.batsense.net/ForgeFlux/ftest)
-   Status: Usable
-   Description: Compliance checker/test runner for [ActivityPub](https://activitypub.rocks) and by
    extension, [ForgeFed](https://forgefed.org)

The idea is to create something similar to
[matrix-org/sytest](https://github.com/matrix-org/sytest), but for
ActivityPub and ForgeFed. This way, we'll be able to measure how
compliant an implementation is to the specifications, which we hope will
improve interoperability between instances.
