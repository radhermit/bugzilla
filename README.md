This repo is exclusively used for testing [bugbite] against a local Bugzilla instance.

# How to run a local container instance:

- install docker-compose (podman-compose can work as well)
- clone this repo
- run in the repo directory: docker compose up -d

If that completes successfully, the local Bugzilla instance is available with
the following settings:

- web: http://127.0.0.1:8080
- user: bugbite@bugbite.test
- password: bugbite

[bugbite]: <https://github.com/radhermit/bugbite>
