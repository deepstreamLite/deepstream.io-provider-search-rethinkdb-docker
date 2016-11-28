Deepstream.io Searchprovider for RethinkDB
---

This docker image contains the `deepstream.io-provider-search-rethinkdb` package.

## Usage

Simple usage:

```
docker run \
-e DEEPSTREAM_AUTH={"username":"rethinkdb-search"} \
deepstreamio/provider-search-rethinkdb:latest
```

Usage within a `docker-compose.yml` file:

```
deepstream-search-provider:
    image: deepstreamio/provider-search-rethinkdb:latest
    environment:
        - DEEPSTREAM_HOST=deepstream
        - DEEPSTREAM_PORT=6021
        - RETHINKDB_HOST=rethinkdb
        - DEEPSTREAM_AUTH={"username":"rethinkdb-search"}
    depends_on:
        - deepstream
        - rethinkdb
```

## Environment Variables to Configure

| Variable | Default Value |
|---|---|
| `DEEPSTREAM_HOST` | `localhost` |
| `DEEPSTREAM_PORT` | `6020` |
| `DEEPSTREAM_AUTH` | `{"username":"rethinkdb-search-provider"}` |
| `PROVIDER_LISTNAME` | `search` |
| `PROVIDER_LOGLEVEL` | `3` |
| `RETHINKDB_HOST` | `localhost` |
| `RETHINKDB_PORT` | `28015` |
| `RETHINKDB_DATABASE` | `deepstream` |
