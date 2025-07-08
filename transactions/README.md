a txn looked up by cometbft hash including payload and result

```
query MyQuery {
  transactionByHash(
    hash: "365C12FADA373D5CA8C4DFB6E0D8C2168E304A6726DF8FA6002EB7B31A897A35"
  ) {
    success
    result
    jsonContent
    created
  }
}
```
>"created" field is also the cometbft time, not the node system time