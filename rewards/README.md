if you want to get all the rewards that a Xian node got

```
query MyQuery {
  allRewards(condition: {type: "masternode", key: NODE_WALLET_ADDRESS}) {
    edges {
      node {
        value
      }
    }
  }
}

```