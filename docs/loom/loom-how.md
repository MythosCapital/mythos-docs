# How to Stake LOOM with Mythos

*Estimated Time: 10 mins*

You can stake LOOM with Mythos using the LOOM provided [DappChain web interface](https://dashboard.dappchains.com/). To stake, all you need are some LOOM tokens in a supported Ethereum wallet that contains both the LOOM tokens and also a bit of ETH to pay for Ethereum transactions.

>:bulb:NOTE: The private keys to your LOOM do not leave your custody during the delegation process. Mythos will never need to take possession of your LOOM.

## Requirements for Staking
* LOOM Tokens
* An Ethereum Wallet (either [Metamask](https://metamask.io/) or [Ledger](https://www.ledger.com/) - *new*)
* A bit of ETH in your wallet to pay for transactions


##  A NOTE ON LEDGER SUPPORT

Ledger support is now available but is currently in Beta mode. If you choose to use Ledger right now, expect some bumps in the process. (By bumps we mean errors, slowness, and inability to delegate from Ledger, but these errors will NOT result in a loss of LOOM funds)

The Ledger does NOT work through [Metamask's Ledger support](https://medium.com/metamask/metamask-now-supports-ledger-hardware-wallets-847f4d51546), so you'll need to use Ledger directly with the DappChain web interface.

>:bulb: There is a bug in a previous verions of Chrome (Chrome 72) and older Chromium-based browsers (Brave and Opera) that could inhibit Ledger transactions with the LOOM interface. Make sure you update to the latest browser version before you begin.

##  Mythos Staking Tutorial

### 1. Create a PlasmaChain account

Navigate to the [Plasmachain Dashboard](https://dashboard.dappchains.com/en/login) and setup an account. Confirm you've navigated to the correct website by verifying the security certificate (check the padlock symbol next to URL).

![](/images/loom_a_1.png)

Click “New User” to setup your account. (If you already have an account, click "Returning User" and restore account with your 12 word recovery phrase)

You’ll now be instructed to store your 12 word recovery seed phrase. Follow the directions and store these immediately. 

>:bulb:These 12 seed words are the only way to restore your Plasmachain account in the event you lose access. Store them accordingly and do not lose them!

Next, you’ll be asked to confirm three of the 12 words you stored.

### 2. Select your Wallet

After you confirm the seed words you'll need to select your Wallet, either Ledger or Metamask. (Read our [note on Ledger support](#a-note-on-ledger-support))

#### Staking from a Metamask

*[Skip](#staking-from-a-ledger) this section if you are staking from Ledger.*

* Make sure [Metamask](https://metamask.io/) is installed. (There are [many](https://medium.com/@followcoin/how-to-install-metamask-88cbdabc1d28) good [tutorials](https://medium.com/@alias_73214/guide-how-to-setup-metamask-d2ee6e212a3e) on how to [setup](https://blog.wetrust.io/how-to-install-and-use-metamask-7210720ca047) Metamask if this is your first time.) 

* Make sure you have LOOM tokens in your Metamask wallet along with enough ETH gas for a few transactions. 

* Make sure you are logged into Metamask. 

![](/images/loom_1.png)


*Above: Metamask wallet with ETH for gas and LOOM ready to stake*

Now, select Metamask "Connect and sign via your browser extension". 

![](/images/loom_a_3.png)

After selecting, you may be prompted to connect your PlasmaChain account to your Ethereum address on the Ledger. Click "Connect" on the Metamask dialog to do so.

![](/images/loom_3.png)

Awesome! You have connected your PlasmaChain account to your Metamask wallet. You are now ready to deposit LOOM tokens into the Plasmachain.


#### Staking from a Ledger

*[Ignore](#3-deposit-loom-into-the-plasmachain) this section if you are staking from Metamask.*

* First, you'll need to ensure your Ledger is updated to the [latest Firmware version](https://support.ledger.com/hc/en-us/articles/360002731113-Update-device-firmware) and [Ethereum wallet app](https://support.ledger.com/hc/en-us/articles/360009576554-Ethereum-ETH-) via the Ledger Live application. 

* Make sure you have LOOM tokens in your Ledger Ethereum wallet along with enough ETH gas for a few transactions.

* Make sure your Ledger is connected to your machine via USB.

* Make sure you have "[Contract data](https://support.ledger.com/hc/en-us/articles/360008268594-Set-up-and-use-MyCrypto)" on in your Ledger under the Ethereum app settings.

* Make sure you have "Display data" off in your Ledger under the Ethereum app settings. 

* Make sure you are using a supported browser, an older version of Chrome (not Chrome 72), or an older version of Opera or Brave. You may decide to [downgrade your browser](https://www.google.com/search?q=Downgrading+chrome&rlz=1C5CHFA_enUS751US753&oq=Downgrading+chrome&aqs=chrome..69i57j0l5.2817j0j1&sourceid=chrome&ie=UTF-8).

Now, select Ledger "Connect and sign via your hardware wallet". 

![](/images/loom_a_2.png)

You should now see a list of Ethereum wallets on your Ledger. 

>:bulb: There are two types of Ledger Ethereum address formats. "Ledger (Legacy)" was previously default for Ledger devices. The second type "Ledger Live" is now the default Ethereum address when setting up via the Ledger Live application.

If you do not see your Ethereum address under "Ledger (Legacy)" switch to "Ledger Live" by editing the "Ledger (Legacy)" textbox and selecting "Ledger Live" to load additional Ethereum addresses.

Once you find your Ethereum address, select it and click Proceed.

Awesome! You have now connected your PlasmaChain account to your Ledger. You are now ready to deposit LOOM tokens into the Plasmachain.

### 3. Deposit LOOM into the Plasmachain

After creating your account and selecting your wallet you will be taken to the [Plasmachain Account](https://dashboard.dappchains.com/account) page. 

Now you'll need to connect to the Plasmachain by mapping to your wallet account. Click “Map Accounts” and sign the corresponding transaction to complete the mapping. 

* If using Metamask, confirm the transaction on Metamask popup dialog
* If using Ledger, approve the "Sign the message" transaction on Ledger interface

![](/images/loom_4.png)

Now, type in the amount of LOOM you want to stake next to the Deposit button. When complete click “Deposit” and confirm the transaction(s).

* If using Metamask, confirm the first transaction, wait until it completes, then confirm the second transaction in Metamask dialog after it pops up. 

* If using Ledger, a transaction approval will appear on the Ledger interface. Depending on your settings, several approvals may be required. Review details and approve.

>:bulb: Metamask Transaction: Your first transaction may take a few minutes to process. After this transaction processes, a second contract transaction will require your approval via Metamask. 

>:bulb: Gas Fee on Ledger: There is no option to manually select gas for transaction, but gas charges were minimal during our tests ranging from 0.0000943908 to 0.000136728 ETH. 

*Having difficulties with Ledger? See [Troubleshooting Ledger](#ledger-troubleshooting-tips) section.*

Once the deposit transactions process, the amount of LOOM in the Dappchain portion of the header will increment to reflect the amount you just deposited.

![](/images/loom_5.png)

Ok, your LOOM is in the Dappchain. You are ready to Stake.


### 4. Delegate to Mythos

Now click [“Validators”](https://dashboard.dappchains.com/validators) in the left navigation panel of the Dashboard and select “Mythos”. Once the Mythos validator page loads you’ll see a “Delegate” button. Click it, select the amount you wish to Delegate, and your preferred Locktime / Bonus. The greater the Locktime / Bonus, the more LOOM rewards you will receive. 

>:bulb:See [LOOM Overview](../  #staking-returns) for details on how Locktime affects your returns.

Click "Delegate" again once you have filled in the amount and selected your Locktime.

![](/images/loom_6.png)

**Congratulations!** Your LOOM stake to Mythos is now in queue. 

Once the next election cycle completes your LOOM will be successfully staked with Mythos. You can monitor the election cycle countdown in the top left of the Plasmachain dashboard.

### 5. Confirm Delegation

After the election cycle is complete confirm your Delegation by clicking the [“My Delegations”](https://dashboard.dappchains.com/delegations) link. There you will see the details of your Delegation.

![](/images/loom_7.png)

Great work. Mythos is glad to have you as a delegate!

If you haven't already done so, take a minute to signup for our [newsletter](https://mythos.services/sign-up/) so you don't miss any LOOM related updates.

## About Rewards and Withdrawals

Every two week cycle you can expect to receive staking rewards denominated in LOOM. You can withdraw your rewards on the [Rewards page](https://dashboard.dappchains.com/rewards) at any time after they are available. 

>:bulb:To maximize your returns and compound them, we recommend you stake your rewards with Mythos or another qualified validator as soon as you receive them.

## About Unstaking

You can also un-delegate from Mythos through the Dashboard. However, remember that your locktime period will influence when you can withdrawal your staked LOOM tokens. Any LOOM that is locked cannot be withdrawn until the locking period has expired. 

## About Changing Validators

LOOM will be adding the ability to change validators during your locktime period so that you're not locked into a specific validator for the duration of your locktime. Stakers will have the ability switch their LOOM stake from one validator to another for any reason. Switching will likely occur during bonding periods every two weeks. 

## Ledger Troubleshooting & Tips 

Ledger support is a bit rough right now, but both LOOM and Ledger are actively working to address. Here are some issues we ran into when staking from a Ledger.

**A Ledger transaction did not appear when attempting to Deposit to Plasmachain** 

Make sure you are running the latest Ledger firmware and have installed the latest Ethereum wallet from the newest version of Ledger Live. Make sure Contract data is set to On in your Ledger application settings. Also, make sure you are not using Chrome 72 or a Chromium version in Opera or Brave that is currently broken with Ledger. 

We had the most success using Ledger with an older version of Opera.

**When depositing to Plasmachain, Ledger is prompting me for too many transaction and parameter confirmations**

This will occur if you have Display data set to On in your Ledger application. The multiple parameter requests on Ledger interface seem to cause a timeout which triggers an error when depositing to Plasmachain. To resolve, turn Display data to Off in Ledger by navigating to Settings in the Ledger Ethereum application and try again.

**Stalled on "Please be patient, Loomy is on it" after approval of deposit transaction on Ledger**

It may take several minutes for the Ethereum transaction to be included in a block. During this time the "Please be patient..." Loomy message will be displayed. 

To see the status of your transaction, go to [Etherscan](https://etherscan.io/) and look up your Ethereum address. You should see a LOOM transaction with a pending status. After this transaction is successful your LOOM deposit should appear in the Plasmachain.

**Interface in Ledger stalls or becomes slow to respond**

We experienced some slowness in the Ledger interface while connected to the Dappchain using a Ledger. In general, the slowness was temporarily resolved by removing the Ledger and re-logging into the Plasmachain. 

You may find it takes several logins to complete your interaction with the Dappchain using a Ledger. We expect future updates will resolve this.

## Need Additional Help?

If you need help, one of our agents will be happy to assist you, just [contact us](https://mythos.services/contact/).

Alternatively, contact LOOM support via [support@loomx.io](mailto:support@loomx.io) or [LOOM telegram](https://t.me/loomnetwork).



<br/> <br/>