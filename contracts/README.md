If you want to retrieve details about one xsc0001-compliant contract

```
query MyQuery {
  contractByName(name: "rewards") {
    txHash
    xsc0001
    code
    created
    name
  }
}
```
if you want to get names of deployed xsc0001-compliant contracts
```
query MyQuery {
  allContracts(condition: {xsc0001: true}) {
    edges {
      node {
        name
      }
    }
  }
}
```