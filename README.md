# README

## Installation

Pull the image `timonier/mailcatcher`:

```sh
# Get the latest image (version 0.6.4)
docker pull timonier/mailcatcher

# Or get a specific version

# Get the version 0.6.4
docker pull timonier/mailcatcher:0.6.4
```

## Usage

Run the application via `docker run`. The mailcatcher options can be passed as arguments:

```sh
# See all mailcatcher options
docker run \
    -i \
    -t \
    --net host \
    timonier/mailcatcher --help

# Run mailcatcher
docker run \
    -i \
    -t \
    --net host \
    timonier/mailcatcher --smtp-port 25 --http-port 80 --ip 0.0.0.0
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [command "docker pull"](https://docs.docker.com/reference/commandline/pull/)
* [command "docker run"](https://docs.docker.com/reference/run/)
* [image "timonier/mailcatcher"](https://hub.docker.com/r/timonier/mailcatcher/)
* [mailcatcher](https://mailcatcher.me/)
