# How to Switch your Stake to Mythos

*Estimated Time: 3 mins*

You can switch your staked ATOMs from your current validator to Mythos with a single CLI command. For this tutorial we assume:

* You have [setup your Cosmos CLI](/cosmos/cosmos-how/#1-prepare-your-cli-environment)
* You have some number of ATOMs staked with an existing Cosmos validator
* You want to switch all or a portion of your ATOMs to Mythos

## Re-Delegating Command

You can re-delegate already staked ATOMs to switch from one validator to another at any time. 

*Notice that re-delegating is different than [un-bonding](/cosmos/cosmos-faq/#5-how-long-does-it-take-to-unbound-my-atoms-once-staked). Unbounding ATOMs requires a 21 days unbonding period during which time your ATOMs remain illiquid and unavailable to withdraw.*

Unlike un-bonding, re-delegating is instant.

You can re-delegate from one validator to another by running a command similar to this:

```
$ gaiacli tx staking redelegate <src-validator-addr> <dst-validator-addr> <amountToBond> --from <delegatorKeyName>
```

Where ``<src-validator-addr>`` is  validator address you're currently delegated to.

Where ``<dst-validator-addr>`` is the destination validator you'd like to delegate to.

Where ``<amountToBond>`` specifies the number of uAtoms you want to switch.

Where ``<delegatorKeyName>`` is the key name you specified when you imported your Ledger keys.


## Re-Delegating to Mythos Example

For example, to move 100,000 already staked ATOMs from Polychain Labs to Mythos with a delegator keyname of ``MainCosmosAccount`` and with a 1uAtom gas fee you'd run this command:

```
$ gaiacli tx staking redelegate cosmosvaloper16m93gjfqvnjajzrfyszml8qm92a0w67nwxrca7 cosmosvaloper1w42lm7zv55jrh5ggpecg0v643qeatfkd9aqf3f 100000000000 --from MainCosmosAccount --gas auto --gas-prices 1.0uatom --chain-id cosmoshub-1
```


##  Need Additional Help?

If you need help, one of our agents will be happy to assist you, just [contact us](https://mythos.services/contact/).

Additionally, you can try the instructions in the [official guide](https://cosmos.network/docs/gaia/delegator-guide-cli.html).
<br/><br/>
