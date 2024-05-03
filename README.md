This repo is exclusively used for testing [bugbite] against a local Bugzilla instance.

# How to run a local container instance:

- install docker-compose (podman-compose can work as well)
- clone this repo
- run in the repo directory: `docker compose up -d`

If that completes successfully, the local Bugzilla instance is available with
the following settings:

- web: http://127.0.0.1:8080
- user: bugbite@bugbite.test
- password: bugbite

For use with bugbite either export the required settings in the shell:

```shell
export BUGBITE_CONNECTION="bugzilla@http://127.0.0.1:8080/"
export BUGBITE_USER="bugbite@bugbite.test"
export BUGBITE_PASS="bugbite"

# search for bugs created in the past day
bite search -c 1d
```

or pass the values to the related options:

```
bite -c "bugzilla@http://127.0.0.1:8080/" -u bugbite@bugbite.test -p bugbite search -c 1d
```

[bugbite]: <https://github.com/radhermit/bugbite>
