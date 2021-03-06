# Platdot-deploy

## Config Builder

This is a simple CLI tool to help automate deployment of new relayers.

An input JSON config looks like this:

```json
{
  "relayerThreshold": "3",
  "ethchains": [
    {
      "name": "alaya",
      "chainId": "2",
      "endpoint": [
        "http://47.110.34.31:6789",
        "http://localhost:8545"
      ],
      "bridge": "atp1emxqzwmz0nv5pxk3h9e2dp3p6djfkqwn4v05zk",
      "erc20Handler": "atp15nqwyjpffntmgg05aq6u7frdvy60qnm82007q5",
      "http": "true",
      "prefix": "atp",
      "networkId": "201030",
      "relayers": [
        "atp18hqda4eajphkfarxaa2rutc5dwdwx9z5vy2nmh",
        "atp1hfhgzgluf9qneuguyw36jrnnsexn388d2lu6xr",
        "atp1sy2tvmghdv47hwz89yu9wz2y29nd0frr9jzd2m",
        "atp1kaptzrfz7v8w4xn7xw88nuxmt5e5uyvhysxqth",
        "atp1tdk4rtlu3pv440r96hqn8s33et7kn25730tpjr"
      ]
    },
    {
      "name": "platon",
      "chainId": "4",
      "endpoint": [
        "http://47.241.98.219:6789",
        "http://localhost:8546"
      ],
      "bridge": "lat13kpqglnd5xl699smjulk64v048ku7d50p3yntw",
      "erc20Handler": "lat18svtj54uzxpxunu0q63fsenyy66skz2eaw4lz3",
      "http": "true",
      "prefix": "lat",
      "networkId": "210309",
      "relayers": [
        "lat18hqda4eajphkfarxaa2rutc5dwdwx9z54jutyc",
        "lat1hfhgzgluf9qneuguyw36jrnnsexn388dnf2zev",
        "lat1sy2tvmghdv47hwz89yu9wz2y29nd0frruy5445",
        "lat1kaptzrfz7v8w4xn7xw88nuxmt5e5uyvhaxsc5c",
        "lat1tdk4rtlu3pv440r96hqn8s33et7kn257geaedv"
      ]
    }
  ],
  "subChains": [
    {
      "name":       "kusama_kusama",
      "chainId":    "1",
      "endpoint":   [
        "wss://kusama.elara.patract.io",
        "ws://localhost:9944"
      ],
      "multiSigAddress": "FYzLbRnPh7ZRkgDf23oziUzFfpokQzwRqpM9Xc6gMt2i21o",
      "totalRelayer": "5",
      "multiSigThreshold": "3",
      "maxWeight": "22698000000",
      "resourceId": "0x0000000000000000000000000000000000000000000000000000000000000000",
      "destId": "2",
      "relayers": [
        "5CHwt8bFyDLC3MyzPQugmmxZTGjShBW2kFMWiC2kSL5TuJxd",
        "5DtTcR48x8yWkSNwn6G1hjVnY61kCVT2SaGfKfU7WAHRvLKq",
        "5FNTYUQwxjrVE5zRRH1hKh6fZ72AosHB7ThVnNnq9Bv9BFjm",
        "5FnCTkAtgLinh6apZJwTX7n72H1A37MHE6xAXChZDbtUWMSg",
        "5HHGiHzTrdbAUFihSC1pgCER41qdrQSxiEBvDsJ2titfAof2"
      ]
    }
  ]
}
```

This example would result in five configs, one for each relayer, with each containing the three provided chains.

## Build/Install

```
$ make build
```
OR
```
$ make install
```

## Usage
```
$ cfgBuilder <input-file> <output-path>
```