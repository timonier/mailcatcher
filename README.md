# README

Catches mail and serves it

## Installation

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/bin

# Use local installation

sudo bin/installer install

# Use remote installation

curl --location "https://gitlab.com/timonier/mailcatcher/raw/master/bin/installer" | sudo sh -s -- install
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

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a [merge request](https://docs.gitlab.com/ee/user/project/merge_requests/).

__Note 1__: [GitHub repository](https://github.com/timonier/mailcatcher) is a mirror. [Merge request](https://docs.gitlab.com/ee/user/project/merge_requests/) has to be submitted to the [GitLab repository](https://gitlab.com/timonier/mailcatcher).

__Note 2__: Use the script `bin/build-image` to test your modifications locally.

If you like / use this project, please let me known by adding a [★](https://help.github.com/articles/about-stars/) on the [GitHub repository](https://github.com/timonier/mailcatcher) or on the [GitLab repository](https://gitlab.com/timonier/mailcatcher).

## Links

* [image "timonier/mailcatcher"](https://hub.docker.com/r/timonier/mailcatcher/)
* [sj26/mailcatcher](https://github.com/sj26/mailcatcher)
* [timonier/dumb-entrypoint](https://gitlab.com/timonier/dumb-entrypoint)
* [timonier/version-lister](https://gitlab.com/timonier/version-lister)
