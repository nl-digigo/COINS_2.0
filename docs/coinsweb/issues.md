# Known issues

This chapter describes known issues and limitations in the COINS 2.0 release.

## Issue: IDFieldname
IDFieldname should be defined as a subproperty of hasProperties but is not. When using the COINS2 validator coins:StringProperties connected via coins:IDFieldname will not fulfill the coins:propertyBelongsTo cardinality contstraint. The coins:propertyBelongsTo is an inverseProperty of coins:hasProperties. As coins:IDFieldname is not a subproperty of coins:hasProperties the inverse will not be set.
