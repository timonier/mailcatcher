# README

Catches mail and serves it

If you like / use this project, please let me known by adding a ★ on the [GitHub repository](https://github.com/timonier/mailcatcher).

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://github.com/timonier/mailcatcher/raw/master/bin/installer" | sudo sh -s -- install
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `installer` will use in `/usr/local/bin`.

## Usage

Run the command `mailcatcher`:

```sh
# See all mailcatcher options

mailcatcher --help

# Run mailcatcher

mailcatcher --foreground --http-port 80 --ip 0.0.0.0 --smtp-port 25
```

## Links

* [image "timonier/mailcatcher"](https://hub.docker.com/r/timonier/mailcatcher/)
* [sj26/mailcatcher](https://github.com/sj26/mailcatcher)
* [timonier/mailcatcher](https://github.com/timonier/mailcatcher)
