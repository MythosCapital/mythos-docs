# Introduction to COSMOS Validator

Cosmos is a network of independent blockchains connected through the Cosmos Hub. Each blockchain is powered by Tendermint Core, a secure PBFT-like consensus engine. Holders of ATOMs can [stake their ATOMs](cosmos-how/) to Mythos to secure the [Cosmos Hub](https://cosmos.network/) and to earn rewards.

## At a Glance


| Staking Asset | Expected Returns | Reward Schedule | Mythos Fee | Min. Stake |
| ------------ | ------------- | :------------: | :------------: | :------------: |
| [ATOMs](https://messari.io/asset/cosmos) | 7-35% annualized | every block (~5s) | 15% | None |


Mythos Cosmos validator: 

| Staking Address  | Status | Staking |
| :------------ | :------------: | :------------: |
| cosmosvaloper1w42lm7zv55jrh5ggpecg0v643qeatfkd9aqf3f | [Mintscan](https://www.mintscan.io/validators/cosmosvaloper1w42lm7zv55jrh5ggpecg0v643qeatfkd9aqf3f) / [Hubble](https://hubble.figment.network/chains/cosmoshub-1/validators/18C78D135C9D81D74F6234DBD268C47F0F89E844) / [BigDipper](https://cosmos.bigdipper.live/validator/18C78D135C9D81D74F6234DBD268C47F0F89E844) | [Stake Now](cosmos-how/) |18C78D135C9D81D74F6234DBD268C47F0F89E844) |

While all ATOM holders must delegate in order to receive block rewards, the Mythos validator is a premium tier validator optimized for large holders. Our validator provides large holders with the additional security, insight, and support levels required to protect the value of their assets. 

>:bulb:We define large holders as an individual or group with more than 100,000 Atoms.

## Staking Returns

As a holder of ATOMs you'll need to bond your stake to a validator like Mythos to earn rewards. You’ll start receiving rewards as soon as your ATOMs are bonded.


### Rewards

There are two types of rewards for staking:


| Rewards Type | Factors | Denomination | 
| ------------ | ------------- | :------------: |
| Block Provisions <br/>(inflation of ATOM supply) | - Cosmos global inflation rate <br/> - Total amount of ATOMs staked <br/>- Block time interval | ATOMs |
|  Fee Rewards <br/>(transaction fees) | - Number of Cosmos transactions <br/> - Gas Fees paid for Cosmos transactions | ATOMs <br/>(and various tokens) |


>:bulb: Cosmos [global inflation rate](cosmos-faq/#definitions) is adaptive with issuance fluctuating between 7% to 20% of annual supply


>:bulb: During the early phases of Cosmos, Block Provisions will make up the bulk of rewards. As usage of the Cosmos network increases we expect Fee Rewards to make up a larger percentage of total rewards.

### Costs

There are also costs incurred for staking:

| Cost Type | Factors | Denomination | 
| ------------ | ------------- | :------------: |
| Validator Commission <br/>(paid to your validator) | Commission fee charged by your validator | ATOMs <br/>  (and various tokens)  |

These fees ensure validators like Mythos can provide high quality infrastructure and suppport for the Cosmos community.

### Risks

It's important to select a high quality validator because there are risks in staking:

| Risk Type | Description | Penalty | 
| ------------ | ------------- | :------------: |
| Double-sign Slashing | If validator signs block twice, stake bonded to validator is slashed. After this occurs all delegates are automatically unbounded and cannot rebond for a three week period. This can occur if validator keys compromised | - 5% stake slash <br/> <br/> - Opportunity cost of missing rewards during 3-week unbond <br/> |
| Downtime Slashing | If  a validator does not sign a block within 10,000 blocks (which equates to about half a day to a day of consecutive downtime), any stake bonded to validator is slashed and the validator is “jailed” for 10 minutes |  - 0.01% stake slash <br/><br/> - Opportunity cost of missing rewards during  10 mins jailed period |

Fortunately Mythos has developed [systems and procedures](/mythos-standards/) to mitigate the risk of slashing. 

### Net Rewards

The net rewards for staking are:

<code>Net Rewards = (Block Provisions + Fee Rewards) - (Validator Commission) </code>

### Reward Payout

Rewards are paid out on a per block basis, which is generally every 5-7 seconds. Stakers can withdraw or re-bond their rewards as they are accrued.

### Staking Example¶

Say you delegate 100,000 ATOMs to the Mythos validator with commission fee of 15%. Assume 55% of ATOMs are currently staking, a 7% Global Inflation Rate, Average Block Time of 5 seconds, your expected reward return is 10.82% annualized or 10,818 ATOMs per year after validator commission fees. 

And if you automatically re-bond your rewards when they are received, your annualized return increases to 11.43% or 11,425 ATOMs.


## Optimizing Rewards

The best way to optimize rewards is through careful validator selection and to re-bond your rewards frequently. We recommend the following:

1. **Minimize slashing risk** by staking with a diversified portfolio of 3-5 trusted validators with a history of uptime, no jail occurrences, and a setup that maximizes for double sign protection

2. **Ensure a reasonable commission rate** when you select your validators. As with anything, look for reasonable commission costs. The lowest cost providers may not be the highest quality and the highest cost providers may not be efficiently optimized.

3. **Re-Bond often** to compound your rewards. Compounding is the secret to wealth accrual and compounding ATOMs by [re-bonding](cosmos-how/#re-bonding-rewards) your rewards is essential to increase your annualized Cosmos rewards. 


---
[How to stake ATOMs](cosmos-how/)

---

<br/><br/>