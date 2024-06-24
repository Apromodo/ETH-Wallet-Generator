# ETH-Wallet-Generator

Node.js based tool to generate vanity Ethereum addresses

## Features!

- Generate multiple addresses
- Supports Multi-core processors
- Vanity contract address
- Log to file
- Checksum based vanity address

### Installation
```sh
$ npm install -g @apromodo/eth-vanity-wallet-generator
$ cwallet -i deadbeef
```

### Examples

Generate an Ethereum address:
```sh
$ cwallet
```

Generate 10 Ethereum addresses:
```sh
$ cwallet -n 10
```

Generate 10 Ethereum addresses with `deadbeef` as starting characters:
```sh
$ cwallet -n 10 -i deadbeef
```

Generate 10 Ethereum addresses with `DEADBEEF` as the checksum address (case sensitive):
```sh
$ cwallet -n 10 -i DEADBEEF -c
```

Generate an Ethereum address with a vanity contract address:
```sh
$ cwallet -i deadbeef --contract
```

Generate 10 Ethereum addresses with `beef` as ending characters:
```sh
$ cwallet -n 10 -s beef
```

Generate 10 Ethereum addresses with both `dead` as starting and `beef` as ending characters:
```sh
$ cwallet -n 10 -i dead -s beef
```

Log output to a file:
```sh
$ cwallet -n 10 -l
```

Get help:
```sh
$ cwallet -h
```

### Docker usage

Get the image:
```sh
# Build image locally after cloning the repository
$ docker build -t cwallet .

# Or download the image
$ docker pull myetherwallet/vanityeth
```

Usage:
```sh
$ docker run -it cwallet

# Pass additional arguments
$ docker run -it myetherwallet/vanityeth -i deadbeef
```

### Running Locally
To run from source:
```sh
git clone git@github.com:Apromodo/eth-vanity-wallet-generator.git
cd eth-vanity-wallet-generator
npm install
./index.js
```

## License

MIT
