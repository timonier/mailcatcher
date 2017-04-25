# README

Catches mail and serves it

## Installation

Copy `bin/mailcatcher` into your executable folder (like `/usr/local/bin` or `$HOME/bin`):

```sh
sudo curl --location --output /usr/local/bin/mailcatcher "https://github.com/timonier/mailcatcher/raw/master/bin/mailcatcher"
sudo chmod +x /usr/local/bin/mailcatcher
```

Linux users can use the [installer](https://github.com/timonier/mailcatcher/blob/master/bin/installer):

```sh
curl --location "https://github.com/timonier/mailcatcher/raw/master/bin/installer" | sudo sh -s install
```

## Usage

Run the command `mailcatcher`:

```sh
# See all mailcatcher options

mailcatcher --help

# Run mailcatcher

mailcatcher --http-port 80 --ip 0.0.0.0 --smtp-port 25
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

__Note__: Use the script `bin/build` to test your modifications locally.

## Links

* [command "docker run"](https://docs.docker.com/reference/run/)
* [image "timonier/mailcatcher"](https://hub.docker.com/r/timonier/mailcatcher/)
* [sj26/mailcatcher](https://github.com/sj26/mailcatcher)
* [timonier/dumb-entrypoint](https://github.com/timonier/dumb-entrypoint)
* [timonier/version-lister](https://github.com/timonier/version-lister)
