# FRZW Tokenomics

![](../../.gitbook/assets/221230-en.png)

## **Emission rate** <a href="#emission-rate" id="emission-rate"></a>

### **Per block**

| **Metric**             | **Emission/block (FRZW)** | **Emission/day (FRZW)** |
| ---------------------- | ------------------------: | ----------------------: |
| Emission               |                        40 |               1,152,000 |
| Burned Weekly          |                    \~30.1 |               \~866,800 |
| **Effective Emission** |               **\~9.9\*** |         **\~285,199\*** |

{% hint style="info" %}
On August 11, 2022, Chefs implemented some configuration upgrades to take full advantage of MasterChef v2. It eliminates the 45,000 FRZW daily burn for the legacy lottery injections. Those burns will now be handled by MasterChef v2 directly along with the usual weekly FRZW burn. Therefore, the effective emissions are now even lower.
{% endhint %}

In addition to the above, a dynamic amount of FRZW is also [minted to the Dev address](https://bscscan.com/address/0xceba60280fb0ecd9a5a26a1552b90944770a4a0e#tokentxns) at a rate of 9.09%. This means that if 100 FRZW are harvested, then 9.09 FRZW is minted in addition and sent to the Dev Address.

{% hint style="warning" %}
All FRZW minted to the Dev address is burned in the weekly burn and never enters circulation.&#x20;

As such, we haven't included it in the above emission rate.
{% endhint %}

## Distribution <a href="#distribution" id="distribution"></a>

| Distributed to                | <p>Reward/block</p><p>(% of emission)</p> | <p>Reward/block</p><p>(total FRZW)</p> |           Reward/day |
| ----------------------------- | ----------------------------------------: | -------------------------------------: | -------------------: |
| Farms (BSC+ETH)               |                                   \~5.08% |                                 \~2.03 |      58,544 (approx) |
| Farms (Aptos)                 |                                   \~0.19% |                                 \~0.08 |       2,275 (approx) |
| Lottery                       |                                   \~0.35% |                               \~0.1389 |       4,000 (approx) |
| FRZW Syrup Pool               |                                  \~19.13% |                                 \~7.65 |     220,380 (approx) |
| **Total Daily FRZW Emission** |                                           |                                        | **285,199 (approx)** |

## **Other Deflationary Mechanics** <a href="#other-deflationary-mechanics" id="other-deflationary-mechanics"></a>

{% hint style="info" %}
The burning process is currently manual. [View burn transactions here](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82?a=0x000000000000000000000000000000000000dead).
{% endhint %}

As well as the above, FRZW is also burned in the following ways:

* **0.0575%** of every trade made on FRZDEX V2 across:
  * BNB Smart Chain
  * Ethereum
  * Aptos
* **0.016%\~0.06%** of every trade made on FRZDEX StableSwap
* **100%** of FRZW sent to the Dev address
* **100%** of FRZW performance fees from IFOs
* **100%** of FRZW spent on Profile Creation and NFT minting
* **100%** of FRZW bid during Farm Auctions
* **20%** of FRZW spent on lottery tickets
* **20%** of all profits from Perpetual Trading
* **8%** of the Pottery prize pot distributed each week
* **3%** of every BNB Prediction markets round is used to buy FRZW for burning
* **3%** of every FRZW Prediction markets round
* **2%** of every yield harvest from all the flexible staking positions in FRZW pool
* **2%** of every NFT sale on the NFT Market is used to buy FRZW for burning

## Why is the FRZW burn manual?

To hit the ground running, FRZDEX launched as an MVP (minimum viable product) with the MasterChef contract emitting 40 FRZW per block. For that reason, the early team didn't add additional functions such as the ability to customize the FRZW minting logic. The team has been controlling FRZW emissions through a manual burn process by creating two pools in MasterChef v1:

* Legacy Lottery Pool (PID - 137) - burned FRZW from the lottery
* Burn Pool (PID - 138) - burned FRZW per block

These pools work similarly to the farms, where the Chefs can adjust the percentage of the 40 FRZW per block allocated to it after each FRZW emission reduction vote.

**However, in April 2022, FRZDEX migrated to a new MasterChef v2 contract.** The ratio of the FRZW burn per block is finally controlled by a dedicated contract. This allows the burn to be much more accurate.

{% hint style="warning" %}
Due to MasterChef v2 occasionally harvesting the full 40 FRZW per block. The supply shown on the homepage (or some 3rd party trackers) might suddenly jump by several million FRZW.

Don't worry - **EMISSION IS NOW CONTROLLED CAREFULLY BY MASTERCHEF V2. FRZW TO BURN WILL NEVER ACTUALLY ENTERS CIRCULATION!**
{% endhint %}

## How to Confirm FRZW Supply for yourself

To confirm that the circulating FRZW supply shown on the FRZDEX homepage is correct,&#x20;

1. Head to the FRZW token contract on BscScan and [see how much FRZW is held by the Burn Address.](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82#balances) That's the total amount of FRZW that's been burned (removed from circulation FOREVER, and impossible to ever retrieve).
2. Then, subtract this burned amount from the "Total Supply" that BscScan shows.
3. This gives you the actual FRZW supply.



#### **Read more about FRZW's deflationary mechanics on the next page.** <a href="#read-more-about-cakes-deflationary-mechanics-on-the-next-page" id="read-more-about-cakes-deflationary-mechanics-on-the-next-page"></a>
