# quantum-installer
A script to automate the installation of quantumX

Installing electrumx isn't really straight-forward (yet). You have to install the latest version of Python and various dependencies for
one of the database engines. Then you have to integrate electrumx into your init system.

`electrumx-installer` simplifies this process to running a single command. All that's left to do for you
is to customise the configuration and to start electrumx.

## Usage
This installs electrumx using the default options:

    wget https://raw.githubusercontent.com/johiruddinsultan/quantum-installer/master/bootstrap.sh -O - | bash

You can also set some options if you want more control:

| -d --dbdir | Set database directory (default: /db/) |
|------------|----------------------------------------|
| --update   | Update previously installed version    |
| --leveldb  | Use LevelDB instead of RocksDB         |

For example:

    wget https://raw.githubusercontent.com/johiruddinsultan/quantum-installer/master/bootstrap.sh -O - | bash -s - -d /media/ssd/electrum-db

     
If you prefer a different operating system that's not listed here, see
[`distributions/README.md`](https://github.com/johiruddinsultan/quantum-installer/blob/master/distributions/README.md) to find out how to add it.
Or open an [issue](https://github.com/johiruddinsultan/quantum-installer/issues/new) if you'd rather not do that yourself.
