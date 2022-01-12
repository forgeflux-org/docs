+++
title = "October 2020"
weight = 40
+++

# October 2020
In the month of October, there were significant changes to the development in ForgeFedv2.
Starting off with the addition of the [OpenAPI Specification](https://forgeflux-org.github.io/northstar/) for Northstar.

## Northstar
A database model was created to store the details of the various forge interfaces,
having these details would be a prerequisite to looking up a server.

Endpoints were subsequently created, following the defined OpenAPI specification.
While the Lookup service was in the process of development, terminologies and the
concept for Forge Federation was also being [discussed](https://github.com/forgeflux-org/spec/tree/master/rfc).

Docker support as part of the CI process was added into the mix.
Keeping in mind, that the test suite was the method to work with the application for
the time being, an initial working model for the lookup service was established.

## Interface
Development of the `libgit` library had begun.
[libgit] is a library that processes the contributor's changes, and generates a patch.
Details regarding the implementation and feature set of libgit will be covered in another section.


## References
- Database Initialization :: [database init](https://github.com/forgeflux-org/northstar/commit/6a82a1bc83d4733a5a077e33ad0c222aed496145)
