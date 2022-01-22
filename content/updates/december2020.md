+++
title = "December 2020"
weight = 40
+++

# December 2020

A test suite was developed for the Gitea ecosystem, and a refactor was performed on the
various structures to leverage the functionality provided by [dataclasses](https://docs.python.org/3/library/dataclasses.html).

Error handling was set up for the client side, and an implementation of a forking
mechanism was developed, followed by the forking mechanism for the Gitea forge.

An authentication mechanism was developed to implement Matrix's [signed JSON](https://github.com/matrix-org/python-signedjson)
feature, but, was later replaced in favor of [HTTP Signatures](https://tools.ietf.org/html/draft-cavage-http-signatures).

