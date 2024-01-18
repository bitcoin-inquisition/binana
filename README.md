# Bitcoin Inquisition Numbers And Names Authority

This repo assigns unique identifiers to proposed changes to Bitcoin.
Identifiers take the form "BIN-YYYY-NNNN" where YYYY is a four digit year,
and NNNN is a four digit identifier. A particular revision of a proposal
may be identified by appending "-RRR", the three digit revision number.

## 2024 Identifiers

| Identifier    | Status     | Name
|:--------------|:-----------|:-----
| BIN-2024-0001 | Draft      | [`OP_CAT`](2024/BIN-2024-0001.md)
| BIN-2024-0002 | Active     | [Heretical Deployments](2024/BIN-2024-0002.md)
| BIN-2024-0003 | Draft      | [`CHECKSIGFROMSTACK`](2024/BIN-2024-0003.md)

## Notes

Proposal identifiers can be converted into a 27 bit numeric identifier as follows:

```c
    id = ((year % 32) << 22) | ((number % 16384) << 8) | (revision % 256)
```

In general, identifiers will be assigned very liberally, with proposals
only being rejected if they are spam, duplicates, or unrelated to
Bitcoin. The assignment of an identifier does not indicate endorsement, or
that a change would be an improvement, or even that a change is possible.
