to query trade transactions from a specific address

```
query MyQuery {
  allEvents(
    condition: {signer: SPECIFIC_ADDRESS, contract: "con_pairs", event: "Swap"}
  ) {
    edges {
      node {
        data
        txHash
        created
        transactionByTxHash {
          success
          result
        }
      }
    }
  }
}

```

show trades for a specific pair

```
query MyQuery {
  allEvents(
    condition: {contract: "con_pairs", event: "Swap"}
    filter:{ dataIndexed:{ contains:{ pair:"PAIR_ID" } } }
  ) {
    edges {
      node {
        data
        txHash
        created
        transactionByTxHash {
          success
          result
        }
      }
    }
  }
}
```