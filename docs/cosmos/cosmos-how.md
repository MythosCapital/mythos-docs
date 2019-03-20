# How to Stake ATOMS with Mythos

*Estimated Time: 10 mins*

Currently you can stake ATOMs with Mythos through a Command Line Interface (CLI) on Windows, MacOS, or Linux. In the future you’ll be able to stake via the official [Cosmos Wallet](https://github.com/cosmos/voyager) and also directly through the [Mythos website](https://mythos.services/cosmos) using a Ledger wallet.

>:bulb: The Cosmos Wallet has not yet passed its security audit, so is currently not recommended for staking. We expect Cosmos to add staking support from its Wallet soon.



## Requirements for Staking
* ATOM Tokens
* A [Ledger](https://www.ledger.com/) hardware wallet

*Note: Since ATOMs are not yet available on exchanges and cannot yet be transferred stakers must have ATOMs from Cosmos Fundraiser in Genesis file in order to stake*

>:bulb:NOTE: The private keys to your ATOMs do not leave your custody during the delegation process. Mythos will never need to take possession of your ATOMs.

## Staking ATOMs via CLI

We assume the following in this tutorial:

* Using Windows, MacOS, or Linux
* Staker has ability to run commands via Command-Line interface
* Staker has a Ledger hardware wallet

### Note for Fundraiser participants

>Cosmos had a [fundraiser](https://fundraiser.cosmos.network/) that ended on April 6th 2017. If you participated you can access your ATOMs on a Ledger using the seed words (12 words) that you generated in the fundraiser event. You can do this on blank Ledger by choosing the “Restore Configuration” option during Ledger setup and entering in your Cosmos seed words. 

>Alternately, if you have an existing Ledger you can reset the device (make sure you back up your Ledger seed words in case of error) and enter your Cosmos seed words when prompted to “Enter your recovery phrase”.


## 1. Prepare your CLI environment

You’ll need the Cosmos SDK including ```gaidd``` and ```gaiacli``` installed in order to delegate via CLI. To install, please follow the Gaia [installation instructions here](https://cosmos.network/docs/gaia/installation.html#install-gaia).

After installation confirm you have successfully installed ```gaia``` by running this command: 

```
$ gaiacli version --long
```

The output should resemble something similar to this:

```
➜ cosmos-sdk: 0.33.0
git commit: 7b4104aced52aa5b59a96c28b5ebeea7877fc4f0
vendor hash: 5db0df3e24cf10545c84f462a24ddc61882aa58f
build tags: netgo ledger
go version go1.12 linux/amd64
```


## 2. Prepare your Ledger and Import Keys


To prepare your Ledger for delegation, you must have the latest version of [Ledger Live](https://www.ledger.com/pages/ledger-live) software installed. Once Ledger Live in installed and updated, connect your Ledger via USB and ensure the Ledger device itself is upgraded to the latest firmware.

Now, go to the Ledger Live Manager and download the “Cosmos” application. This will take a few moments.

![](/images/cosmos_1.png)

Once the Cosmos application is installed, you can navigate to the application using the interface on your Ledger to verify it has successfully installed.

Leave the Ledger Connected and open the Cosmos application using your Ledger. 

![](/images/cosmos_2.jpg)

Next, determine a name for your Cosmos Ledger keys and import the keys from your Ledger by running the following: 

```
$ gaiacli keys add <keyName> --ledger
```

In place of ``<keyName>`` specify a name for your Cosmos Ledger keys, for example: ``MainCosmosAccount``

Check the accounts you have imported by running the following command:

```
$ gaiacli keys list
```

The output should resemble something similar to this:

```
➜ NAME: TYPE: ADDRESS:     PUBKEY:
MainCosmosAccount    ledger    cosmos1w42lm7zv55jrh5ggpecg0v643qeatfkdqf5ua6    cosmospub1addwnpepqfgfdpgjpqr9grjhvwhylqt3cldfkmnknl9tf2g0dtd0qh4vumfe5rqz57v
```

*Note: The address that begins with ``cosmos1`` is your public key.*

Great! Your Ledger is now setup and ready to delegate ATOMs.

### 3. Connect to Node and Configure Connection

Run the following command to connect to Mythos Cosmos full node:

```
$ gaiacli config node cosmoshub-1.mythos.services:26657
```

Now configure your connection by running the following: 

```
$ gaiacli config trust-node false
```

Ok, you are connected to the Mythos full node.

### 4. Determine Amounts and Run Delegation Command

It's time to determine the amount of ATOMs you want to stake and set the gas price for your delegation transaction.

*Example:*

* *100000000000uatoms to delegate (which is 100,000 Atoms)*
* *1uatom as gas price (gas price can be minimal)*

>:bulb: Units are specified in uAtoms which is 1 millionth of an Atom. In order to convert an uAtom to an Atom divide the uAtom by 1,000,000. (E.g. 1,000,000 uAtoms = 1 Atom)

*Note: Don’t delegate the full amount from your account. You’ll want to keep an ATOM or so in your account to pay for gas fees which are required to withdraw and re-bond rewards*

Once you’ve determined your staking amount, you can stake to Mythos by running a command similar to the following:

```
$ gaiacli tx staking delegate <validatorAddress> <amountToBond>uatom --from <delegatorKeyName> --gas auto --gas-prices <amountGas>uatom --chain-id cosmoshub-1
```

* For``<validatorAddress>`` use the Mythos validator address ``cosmosvaloper1w42lm7zv55jrh5ggpecg0v643qeatfkd9aqf3f`` 
* For ``<amountToBond>`` specify the number of uAtoms to delegate. 
* For``<delegatorKeyName>`` use the key name you specified when you imported your Ledger keys (e.g. ``MainCosmosAccount``)
* For ``<amountGas>`` add the gas price in uAtoms (1uAtom is probably sufficient)

For example, to delegate 100,000 ATOMs to Mythos at a 1uAtom gas fee you'd run:

```
$ gaiacli tx staking delegate cosmosvaloper1w42lm7zv55jrh5ggpecg0v643qeatfkd9aqf3f 100000000000uatom --from MainCosmosAccount --gas auto --gas-prices 1uatom --chain-id cosmoshub-1
```

Congrats! If you've successfully run this command you are now staking with Mythos.

### Confirming your stake

You can search for your Cosmos address in [Mintscan](https://www.mintscan.io/) to see the staking transaction and your account details.


## Withdrawing rewards

Rewards are accrued on a per block basis and you can withdraw your rewards at any time. 
 
The command to withdraw rewards is: 

```
$ gaiacli tx distr withdraw-all-rewards --from <delegatorKeyName>
``` 

Where ``<delegatorKeyName>`` is the key name you specified when you imported your Ledger keys.


## Re-bonding Rewards

You'll want to re-bond your rewards on a frequent basis in order to compound your returns. While automated re-bonding capabilities will be added to wallets soon, for now you'll need to manually [withdraw your rewards](#withdrawing-rewards) and use the [instructions above](#4-determine-amounts-and-run-delegation-command) to bond your rewards.


##  Need Additional Help?

If you need help, one of our agents will be happy to assist you, just [contact us](https://mythos.services/contact/).

Additionally, you can try the instructions in the [official guide](https://cosmos.network/docs/gaia/delegator-guide-cli.html).
<br/><br/>