# FRZW Tokenomics v1

![](../../.gitbook/assets/en-1129.png)

## **Emission rate** <a href="#emission-rate" id="emission-rate"></a>

### **Per block**

| **Metric**                                                                   | **Emission/block (FRZW)** | **Emission/day (FRZW)** |
| ---------------------------------------------------------------------------- | ------------------------: | ----------------------: |
| Emission                                                                     |                        40 |               1,152,000 |
| Burned Weekly [(PID 138)](cake-tokenomics-v1.md#why-is-the-cake-burn-manual) |                    -25.75 |                -787,600 |
| **Effective Emission**                                                       |              **<14.25\*** |           **364,400\*** |

\*Effective Emission is in fact slightly below this amount: an additional 45,000 FRZW per day is diverted from the amount allocated to the lottery, and burned (PID 137 - Details below).

In addition to the above, a dynamic amount of FRZW is also [minted to the Dev address](https://bscscan.com/address/0xceba60280fb0ecd9a5a26a1552b90944770a4a0e#tokentxns) at a rate of 9.09%. This means that if 100 FRZW are harvested, then 9.09 FRZW is minted in addition and sent to the Dev Address.

{% hint style="info" %}
All FRZW minted to the Dev address is burned in the weekly burn and never enters circulation.&#x20;

As such, we haven't included it in the above emission rate.
{% endhint %}

## Distribution <a href="#distribution" id="distribution"></a>

| Distributed to                | Reward/block (% of emission) | Reward/block (total FRZW) |           Reward/day |
| ----------------------------- | ---------------------------: | ------------------------: | -------------------: |
| Farms and Lottery             |                       10.62% |                      4.25 |     122,400 (approx) |
| of which diverted and burned  |                              |                           |              -46,000 |
| Syrup Pools                   |                          25% |                        10 |     288,000 (approx) |
| **Total Daily FRZW Emission** |                              |                           | **364,400 (approx)** |

## **Other Deflationary Mechanics** <a href="#other-deflationary-mechanics" id="other-deflationary-mechanics"></a>

{% hint style="info" %}
The burning process is currently manual. [View burn transactions here](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82?a=0x000000000000000000000000000000000000dead).
{% endhint %}

As well as the above, FRZW is also burned in the following ways:

* **0.05%** of every trade made on FRZDEX V2
* **100%** of FRZW sent to the Dev address
* **100%** of FRZW performance fees from IFOs
* **100%** of FRZW spent on Profile Creation and NFT minting
* **100%** of FRZW bid during Farm Auctions
* **20%** of FRZW spent on lottery tickets
* **45,000** FRZW per day (historically assigned to the lottery) (_The FRZW for this is generated by a farm - PID 137)_
* **3%** of every Prediction markets round is used to buy FRZW for burning
* **2%** of every yield harvest in the Auto FRZW Pool
* **2%** of every NFT sale on the NFT Market is used to buy FRZW for burning

## Why is the FRZW burn manual?

To hit the ground running, FRZDEX launched as an MVP (minimum viable product) with the MasterChef contract emitting 40 FRZW per block. For that reason, the early team didn't add additional functions such as the ability to customize the FRZW minting logic. As migrating to a new MasterChef would require a lot of time and effort, the team opted to reduce FRZW emissions instead through a manual burn process by creating two pools:

* Legacy Lottery Pool (PID - 137) - burned FRZW from the lottery
* Burn Pool (PID - 138) - burned FRZW per block

These pools work similarly to the farms, where the Chefs can adjust the percentage of the 40 FRZW per block allocated to it after each FRZW emission reduction vote.

{% hint style="warning" %}
On the day of the burn, the supply shown on the homepage might suddenly jump by several million FRZW.&#x20;

Don't worry - **THIS FRZW NEVER ACTUALLY ENTERS CIRCULATION:**
{% endhint %}

This apparent jump is just because of how all the FRZW that's allocated for the burn is stored during the week.&#x20;

The FRZW sent to both pools PID-137 and PID-138 are harvested before completing the weekly token burns, and this makes the Total Supply shown on the site jumping by \~6M. This is because pending FRZW isn’t registered in the Total Supply until it's harvested on the burn day. Once the token burn transaction is completed, the \~6M is shown in the Burned to Date.&#x20;

## How to Confirm FRZW Supply for yourself

To confirm that the circulating FRZW supply shown on the FRZDEX homepage is correct,&#x20;

1. Head to the FRZW token contract on BscScan and [see how much FRZW is held by the Burn Address.](https://bscscan.com/token/0x0e09fabb73bd3ade0a17ecc321fd13a19e81ce82#balances) That's the total amount of FRZW that's been burned (removed from circulation FOREVER, and impossible to ever retrieve).
2. Then, subtract this burned amount from the "Total Supply" that BscScan shows.
3. This gives you the actual FRZW supply.



#### **Read more about FRZW's deflationary mechanics on the next page.** <a href="#read-more-about-cakes-deflationary-mechanics-on-the-next-page" id="read-more-about-cakes-deflationary-mechanics-on-the-next-page"></a>
