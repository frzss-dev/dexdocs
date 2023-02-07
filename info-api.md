# Info API

## Documentation

All FRZDex pairs consist of two different tokens. FRZSS is not a native currency in FRZDex, and is represented only by WFRZSS in the pairs.

The canonical WFRZSS address used by the FRZDex interface is `0xb92e3252ead5d78ace9f5b415b71afe754136121`.

Results are cached for 5 minutes (or 300 seconds).

### [`/summary`](https://api.frzdex.com/api/summary)

Returns data for the top \~1000 FRZDex pairs, sorted by reserves.

#### Request

`GET https://api.frzdex.com/api/summary`

#### Response

```json5
{
  "updated_at": 1234567,              // UNIX timestamp
  "data": {
    "0x..._0x...": {                  // ERC20 token addresses, joined by an underscore
      "price": "...",                 // price denominated in token1/token0
      "base_id": "...",           	  // id of token0
      "base_name": "...",             // name of token0
      "base_symbol": "...",           // symbol token0
	  "quote_id": "...",           	  // id of token1
      "quote_name": "...",            // name of token1
      "quote_symbol": "...",          // symbol token1
      "base_volume": "...",           // last 24h volume denominated in token0
      "quote_volume": "..."           // last 24h volume denominated in token1
    },
    // ...
  }
}
```

### [`/tokens`](https://api.frzdex.com/api/tokens)

Returns the tokens in the top \~1000 pairs on FRZDex, sorted by reserves.

#### Request

`GET https://api.frzdex.com/api/tokens`

#### Response

```json5
{
  "updated_at": 1234567,              // UNIX timestamp
  "data": {
    "0x...": {                        // the address of the ERC20 token
      "name": "...",                  // not necessarily included for ERC20 tokens
      "symbol": "...",                // not necessarily included for ERC20 tokens
      "price": "...",                 // price denominated in USD
      "price_FRZSS": "...",             // price denominated in FRZSS
    },
    // ...
  }
}
```

### [`/tokens/0x...`](https://api.frzdex.com/api/tokens/0x0E09FaBB73Bd3Ade0a17ECC321fD13a19e81cE82)

Returns the token information, based on address.

#### Request

`GET https://api.frzdex.com/api/tokens/0x0E09FaBB73Bd3Ade0a17ECC321fD13a19e81cE82`

#### Response

```json5
{
  "updated_at": 1234567,              // UNIX timestamp
  "data": {
    "name": "...",                    // not necessarily included for ERC20 tokens
    "symbol": "...",                  // not necessarily included for ERC20 tokens
    "price": "...",                   // price denominated in USD
    "price_FRZSS": "...",               // price denominated in FRZSS
  }
}
```

### [`/pairs`](https://api.frzdex.com/api/pairs)

Returns data for the top \~1000 FRZDex pairs, sorted by reserves.

#### Request

`GET https://api.frzdex.com/api/pairs`

#### Response

```json5
{
  "updated_at": 1234567,              // UNIX timestamp
  "data": {
    "0x..._0x...": {                  // the asset ids of FRZSS and ERC20 tokens, joined by an underscore
      "pair_address": "0x...",        // pair address
      "base_name": "...",             // token0 name
      "base_symbol": "...",           // token0 symbol
      "base_address": "0x...",        // token0 address
      "quote_name": "...",            // token1 name
      "quote_symbol": "...",          // token1 symbol
      "quote_address": "0x...",       // token1 address
      "price": "...",                 // price denominated in token1/token0
      "base_volume": "...",           // volume denominated in token0
      "quote_volume": "...",          // volume denominated in token1
      "liquidity": "...",             // liquidity denominated in USD
      "liquidity_FRZSS": "..."          // liquidity denominated in FRZSS
    },
    // ...
  }
}
```
