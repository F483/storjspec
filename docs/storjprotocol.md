# Storj core protocol layer

[Python reference implimentation](https://github.com/storj/storjprotocol)


## Contract version 0 specification

| Property  |      Type             | Description                               |
|-----------|:---------------------:|:-----------------------------------------:|
| version   | integer               | Must be 0                                 |
| renterid  | string                | 160bit base58 encoded                     |
| farmerid  | string                | 160bit base58 encoded                     |
| shardid   | string                | 160bit base58 encoded                     |
| shardsize | integer               | In bytes as a power of two.               |
| begin     | integer               | Unixtime when the contract begins         |
| duration  | integer               | Contract duration in seconds              |
| end       | integer               | Unixtime when the contract ends           |
| currency  | integer               |                                           |
| amount    | integer               |                                           |
| audits    | [(float, float), ...] | Relative (time, amount), sum must be 1.0  |


## User API

### Validate contract

|           |           |                                   |
|-----------|-----------|-----------------------------------|
| Command   | validate  |                                   |
| Arguments | contract  | The contract to be validated.     |
| Returns   | bool      | True if the contract is valid.    |
| Raises    |           |                                   |
