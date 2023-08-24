# TokenBook-public

A Token Book meant to store asset information used for collaborative projects with Sphere Finance

## Contributing

You are free to contribute new assets by making PRs.

### Asset addition

1. Introduce token **symbol** & **address** under /tokens/src/**[NETWORK]**
2. Introduce token image as a .svg file. ex: STAR.svg

> [!NOTE]
> symbol must be stored upper case. Address must be a valid hex

## Token

### token images

All token images are fetched via /tokens/images/**[SYMBOL]**.svg

> [!NOTE]
> symbol must always be upper case

### token data

All token data is fetched via /tokens/data/**[chain]**.json

> [!NOTE]
> chain must always be lower case

Token data contains token:

- address,
- symbol,
- name,
- decimals
- image

Tokens are stored in a
`ts Record<address|symbol, { address: string, symbol: string, name: string, decimals: number, image: string }>` format

> [!NOTE]
> address need to be lower case & symbol need to be upper case

example:

```JSON
{
    "0x82af49447d8a07e3bd95bd0d56f35241523fbab1": {
        "address": "0x82af49447d8a07e3bd95bd0d56f35241523fbab1",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "image": "https://raw.githubusercontent.com/WeaverSphere/TokenBook-public/main/tokens/images/WETH.svg",
        "decimals": 18
    },
    "WETH": {
        "address": "0x82af49447d8a07e3bd95bd0d56f35241523fbab1",
        "name": "Wrapped Ether",
        "symbol": "WETH",
        "image": "https://raw.githubusercontent.com/WeaverSphere/TokenBook-public/main/tokens/images/WETH.svg",
        "decimals": 18
    },
}
```
