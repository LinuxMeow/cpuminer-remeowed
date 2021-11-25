## What is cpuminer-remeowed?

cpuminer-remeowed is a fork of cpuminer-gr by WyvernTKC which is a fork of cpuminer-opt by Jay D Dee which is a fork of cpuminer-multi with optimizations
imported from other miners developped by:

- lucas Jones
- djm34
- Wolf0
- pooler
- Jeff garzik
- ig0tik3d
- elmad
- palmd
- and Optiminer

with additional optimizations by Jay D Dee.

## Licensing

All of the code is believed to be open and free as a project linensed under the GPL-2.0 License which is distributed with this project.

## Disclaimer

Miner programs are often flagged as malware by antivirus programs. This is a false positive and they are flagged because of many unauthorised cryptocurrency mining practices by malicious code made by people with malicious intents.

The source code is open for anyone to inspect. If you don't trust the software, do not use it.

## Requirements
1. A x86-64 architecture CPU with a minimum of SSE2 support. Further optimizations are available on some algoritms for CPUs with AES, AVX, AVX2, SHA, AVX512 and VAES. ARM and Aarch64 CPUs are not supported, yet.

2. 64 bit Linux or Windows OS. 64 bit Windows OS is supported with mingw-w64 and msys or pre-built binaries. MacOS, OSx and Android are not supported.

3. Stratum pool supporting stratum+tcp:// or stratum+ssl:// protocols or RPC getwork using http:// or https://.

## Supported Algorithms

| Algorithm    | Description                  |
|--------------|------------------------------|
| allium       | Garlicoin                    |
| anime        | Animecoin                    |
| argon2       | Argon2 coin (AR2)            |
| argon2d250   | argon2d-crds, Credits (CRDS) |
| argon2d500   | argon2d-dyn,  Dynamic (DYN)  |
| argon2d4096  | argon2d-uis, Unitus, (UIS)   |
| axiom        | Shabal-256 MemoHash          |
| blake        | Blake-256 (SFR)              |
| blake2b      | Blake2b 256                  |
| blake2s      | Blake-2 S                    |
| blakecoin    | blake256r8                   |
| bmw          | BMW 256                      |
| bmw512       | BMW 512                      |
| c11          | Chaincoin                    |
| decred       |                              |
| deep         | Deepcoin (DCN)               |
| Dmd-gr       | Diamond-Groestl              |
| ghostrider   | Raptoreum (RTM)              |
| groestl      | Groestl coin                 |
| hex          | x16r-hex                     |
| hmq1725      | Espers                       |
| hodl         | Hodlcoin                     |
| jha          | Jackpotcoin                  |
| keccak       | Maxcoin                      |
| keccakc      | Creative coin                |
| lbry         | LBRY Credits                 |
| luffa        | Luffa                        |
| lyra2h       | Hppcoin                      |
| lyra2re      | lyra2                        |
| lyra2rev2    | lyra2v2                      |
| lyra2rev3    | lyrav2v3                     |
| lyra2z       |                              |
| lyra2z330    | Zoin (ZOI)                   |
| m7m          | Magi (XMG)                   |
| minotaur     | Ringcoin (RNG)               |
| Myr-gr       | Myriad-Groestl               |
| neoscrypt    | NeoScrypt(128, 2, 1)         |
| nist5        | Nist5                        |
| pentablake   | Pentablake                   |
| phi1612      | phi                          |
| phi2         | Luxcoin (LUX)                |
| phi2-lux     | identical to phi2            |
| pluck        | Supcoin                      |
| polytimos    | Ninja                        |
| power2b      | MicroBitcoin (MBC)           |
| quark        | Quark                        |
| qubit        | Qubit                        |
| scrypt       | Scrypt(1024, 1, 1)           |
| scrypt:N     | scrypt(N, 1, 1)              |
| sha256d      | Double SHA-256               |
| sha256q      | Pyrite (PYE)                 |
| sha256t      | Onecoin (OC)                 |
| sha3d        | Double keccak256 (BSHA3)     |
| shavite3     | Shavite3                     |
| skein        | Skein+Sha (Skeincoin)        |
| skein2       | Double Skein (Woodcoin)      |
| skunk        | Signatum (SIGT)              |
| sonoa        | Sono                         |
| timetravel   | Machinecoin (MAC)            |
| timetravel10 | Bitcore                      |
| tribus       | Denarius (DNR)               |
| vanilla      | blake256r8vnl (VCash)        |
| veltor       | Veltor (VLT)                 |
| verthash     | Vertcoin                     |
| whirlpool    |                              |
| whirlpoolx   |                              |
| x11          | Dash                         |
| x11evo       | Revolvercoin                 |
| x11gost      | sib (SibCoin)                |
| x12          | Galaxie Cash (GCH)           |
| x13          | X13                          |
| x13bcd       | bcd                          |
| x13sm3       | hsr (Hshare)                 |
| x14          | X14                          |
| x15          | X15                          |
| x16r         |                              |
| x16rv2       |                              |
| x16rt        | Gincoin (GIN)                |
| X16rt-veil   | Veil (VEIL)                  |
| x16s         | Pigeoncoin (PGN)             |
| x17          |                              |
| x21s         |                              |
| x22i         |                              |
| x25x         |                              |
| xevan        | Bitsend (BSD)                |
| yescrypt     | Globalboost-Y (BSTY)         |
| yescryptr8   | BitZeny (ZNY)                |
| yescryptr8g  | Koto (KOTO)                  |
| yescryptr16  | Eli                          |
| yescryptr32  | WAVI                         |
| yespower     | Cryply                       |
| yespowerr16  | Yenten (YTN)                 |
| Yespower-b2b | generic yespower + blake2b   |
| zr5          | Ziftr                        |
                           

## Quick Setup

To add or use options from the miner, use included config.json file. All options should be presented in JSON format like:

```json
"long-flag-name": "Some_value"
```

Some examples:

```json
      "tune-full": true
      "tune-config": "some_filename"
      "url": "stratum+tcp://YOUR_POOL_ADDRESS:PORT"
      "user": "YOUR_WALLET.WorkerName"
```

For full miner option list and other tips please read the readme.txt file or run miner with `--help` flag

```sh
./cpuminer-remeowed --help
```

If `cpuminer-remeowed` executable is not present, you can run `--help` flag on any other miner executable located in the binaries directory. Example:

```sh
./cpuminer-avx2 --help
```

## Tuning

Tuning starts automaticaly with the start of the miner. If previous tuning file `tune_config` exists (or `--tune-config=FILE` flag is used), tuning process will be skipped and preconfigured tuning file will be used instead.

This behavior can be overridden by `--no-tune` or `--force-tune`.

| CPU Type | Tuning time  |
|----------|--------------|
| AVX2     | ~155 minutes |
| Other    | ~69 minutes  |

Tuning your CPU is strongly recommended unless you already have preset file to maximise your hashrate.

## Bugs

Users are encouraged to post their bug reports using git issues:

<a href="https://github.com/LinuxMeow/cpuminer-remeowed/issues" target="_blank">https://github.com/LinuxMeow/cpuminer-remeowed/issues</a>

All problem reports must be accompanied by a proper problem definition. This should include how the problem occurred, the command line and
output from the miner showing the startup messages and any errors. A history is also useful, in example if it worked before the issue appeared.

## Donations

Donations are not mandatory, but help me dedicate more time into the project.

Raptoreum:

```txt
RQJtmGLrK1vsSZbQdM9K6g3skvJmRZD5Ug
```

Ravencoin:

```txt
RNp6zqDVKA2r1QeiJTr1Yuiz6PS9Frt5rW
```

Ergo:

```txt
9h4uH3fu47cfovtidorDpFFuLyqWbnkJ9UZRLKcxXcBhkCUa27X
```

This fork introduces default of 1% donation on Ghost Rider (GR) algorithm only. It can be turned off in the source code. It can be set in the `config,json` file by adding `donation` key.

```json
"donation": 1.0
```
