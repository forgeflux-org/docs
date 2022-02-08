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

## Setting up the Development Environment

In order to test out and utilise the Northstar lookup service, we will need to set
up an interface to be run on the local machine. There are a few configuration 
changes that must be made for the interface to be recognized by the lookup service.

Changes to the `config/settings.toml`,
```toml
[default.system]
northstar = "http://computer.domain.com:port"

[default.server]
url = "http://computer.domain.com:port"
```

Note that the port assigned to the interface and northstar must not already be in
use by another application/service, and that you can find out the hostname for 
your system through the following command,
```sh
hostname --fqdn
```

There are a few more settings to add in, as a means to validate the user who hosts
the interface, this also depends on the forge of your choosing. As of right now,
`interface` supports only gitea, and we can fill up the `config/settings.toml`,
with the same.

```toml
[default]
forge = "gitea"

[default.gitea]
host = "https://gitea.com"
api_key = "generate-the-api-key-from-gitea-and-paste-here"
username = "fluxer101"
password = "flux101"
```

Note that the API key in Gitea is known as an access token, one which can be 
generated [here](https://gitea.com/user/settings/applications).

## FAQ
### Why does an integrity error show up?
As ForgeFlux's Interface is an actively developing project, there are a few 
errors that are caused by an upgrade to the database, in which case integrity errors
are bound to pop up. In this case, remove the `instance/` directory where the database
for the service would be stored, to rebuild it the next time the application is run.
