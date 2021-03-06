[![Pick Axe Version Manager](https://raw.github.com/gevans/pick/master/pickaxe-banner.png)](https://github.com/gevans/pick#readme)

Use `pick` to install, run, and manage your favorite versions and forks of
cgminer. Based on [rbenv](https://github.com/sstephenson/rbenv) where a lot of
this project's code and inspiration comes from.

## Installation

Pick can be automatically installed through
[`pick-installer`](https://github.com/gevans/pick/blob/master/pick-installer):

```sh
$ curl -sSL https://raw.github.com/gevans/pick/master/pick-installer | bash
```

Alternatively, pick can be installed manually:

```sh
$ git clone --recursive https://github.com/gevans/pick.git ~/.pick
$ echo '[ -d "$HOME/.pick/bin" ] && PATH="$HOME/.pick/bin:$PATH"'
```

## Usage

### Installing Miners

```sh
# List supported miners:
$ pick install

# Install a miner:
$ pick install sgminer

# Install a specific version:
$ pick install sgminer 4.1.0

# Specify `./configure` options:
$ pick install cgminer 3.7.2 -- --enable-scrypt
```

### Uninstalling Miners

```sh
# Remove a previously installed miner:
$ pick uninstall cgminer-3.7.2
```

Alternatively, you can look in `$PICK_ROOT/versions/` and `rm -rf` the directory
of the version you want to remove.

### Changing Miners

```
# Use the latest stable release:
$ pick use bfgminer

# Use the latest minor release:
$ pick use sgminer 4.1

# Use a specific release:
$ pick use cgminer 3.7.2
```

### Running Miners

```sh
# Execute the current miner:
$ pick exec -c /path/to/config.json

# Execute the latest stable release:
$ pick exec cgminer -c /path/to/config.json

# Execute a specific release:
$ pick exec bfgminer 3.10.0 -c /path/to/config.json
```

### Updating Pick

```sh
# Update to the latest stable version:
$ pick update master

# Update to the latest development version:
$ pick update develop
```

## Contributing

1. Fork it (http://github.com/gevans/pick/fork)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Obligatory Donation Links

Did this project save you time? Consider sending a beer:

```
BTC: 16eVffBKdDnCFahVA691ENQTyGy5cUtz95
LTC: LiFWkwWzbvdqcb6fC57sEjvCHMizgqG1Wr
```

![Bitcoin](http://i.imgur.com/JupFQXS.png)
![Litecoin](http://i.imgur.com/1eGvltd.png)
