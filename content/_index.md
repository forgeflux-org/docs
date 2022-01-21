+++
title = "Magic Bridges"
insert_anchor_links = "right"
+++

## A day of the past

It's a Friday evening, and you've sat down to work on some code. \
Halfway through testing the code, you realise that there's a problem with a dependency.\

Something's not supposed to work the way it does. \
You hop on to the code-hosting platform, or forge, that you use on a daily basis
and search for the library.

Wait, it's not here? \
You close your eyes, before reluctantly heading over to a search engine,
to find the repository being hosted on another forge that you haven't worked with.

At this point, in order to file a bug report, or even send a Pull Request that could
fix the issue, you would be required to create an account on the forge and clone the
repository and relearn the workings of the particular forge before finally working
on the code.

Manually tracking notifications, setting up new remotes for the upstreams,
configuring GPG and SSH keys, and having to set up a new development workflow. \
The evening continues into the night, and you're finally ready with that PR, which
you had to learn a new forge for.

## A day of the future

Worrying about the forge-specific operations that you'll need to perform are a thing of
the past now. \
With the inclusion of a bridging feature in your code-hosting platform, you can finally
forget about how other forges behave and whether you'll need to work towards creating
a new account to contribute.

A contribution, be it a Bug Report, Feature Request, or a Pull Request, now can be
solved through setting up a bridge to the repository you want to contribute to.

Days are pleasant and you can continue working on your code after you're done with the
issue of the library. \
You check out and have more time for things that you wanted to work on for the rest of
the day.

## Enter ForgeFlux

While the days of the past are what we live in currently, ForgeFlux is the intermediary
that seeks to get developers to the days of the future!

Implementing bridging leveraging the API space, [Northstar](@/services/northstar.md)
points, and the [Interface](@/services/interface.md) sets it all up.

Know more about how ForgeFlux works [here!](@/getting-started/how.md)\
We're currently still in active development, and you can check what we've been
working on, in the `updates/` section.
