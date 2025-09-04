# Bitcoin Inquisition Numbers And Names Authority

This repo assigns unique identifiers to proposed changes to Bitcoin.
Identifiers take the form "BIN-YYYY-NNNN" where YYYY is a four digit year,
and NNNN is a four digit identifier. A particular revision of a proposal
may be identified by appending ".RRR", the three digit revision number.

## 2024 Identifiers

| Identifier    | Status     | Name
|:--------------|:-----------|:-----
| BIN-2016-0118 | Active     | [`SIGHASH_ANYPREVOUT` for Taproot Scripts](2016/BIN-2016-0118.md)
| BIN-2016-0119 | Active     | [`CHECKTEMPLATEVERIFY`](2016/BIN-2016-0119.md)
| BIN-2024-0001 | Active     | [`OP_CAT`](2024/BIN-2024-0001.md)
| BIN-2024-0002 | Active     | [Heretical Deployments](2024/BIN-2024-0002.md)
| BIN-2024-0003 | Draft      | [`CHECKSIGFROMSTACK`](2024/BIN-2024-0003.md)
| BIN-2024-0004 | Draft      | [`OP_INTERNALKEY`](2024/BIN-2024-0004.md)
| BIN-2024-0005 | Info       | [Bitcoin Related Specifications](2024/BIN-2024-0005.md)

## Notes

Proposal identifiers may be minified by omitting the leading dash, using a two digit year, and omitting leading zeroes, eg BIN-2024-0001 becomes BIN24-1, and its third revision, BIN-2024-0001.003 would become BIN24-1.3.

Proposal identifiers can be converted into a 27 bit numeric identifier as follows:

```c
    id = ((year % 32) << 22) | ((number % 16384) << 8) | (revision % 256)
```

In general, identifiers will be assigned very liberally, with proposals
only being rejected if they are spam, duplicates, or unrelated to
Bitcoin. The assignment of an identifier does not indicate endorsement, or
that a change would be an improvement, or even that a change is possible.
