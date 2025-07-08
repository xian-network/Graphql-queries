a list of all NFTs owned by a person
```
query MyQuery {
  allStateChanges(
    filter: {
      key: { startsWith: "con_pixel_frames_info_v0_1", endsWith: "owner" }
      value: {
        equalTo: WALLET_ADDRESS
      }
    }
  ) {
    nodes {
      key
      value
    }
  }
}
```