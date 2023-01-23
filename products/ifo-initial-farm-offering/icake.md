---
description: Fixed-Term FRZW Staking and IFO Allocations
---

# iFRZW

### **What is iFRZW?**

iFRZW is similar to “IFO credits” from the previous IFO FRZW staking pool, which was retired during the MasterChef v2 migration. After this update, iFRZW will determine the maximum FRZW commit limit in the FRZDEX IFO public sales. For example, if you have 200 iFRZW, you will be able to commit 200 FRZW in any upcoming IFO public sales.

**iFRZW is NOT a new token, it is a numerical metric being used by the FRZDEX IFO system.**

### How is iFRZW calculated?

The number of iFRZW you have is based on the number of FRZW staked in the fixed-term FRZW staking pool and the total staking duration of your current fixed-term staking position.

iFRZW works based on a staking duration threshold for all iFRZW users.

If your staking duration is above the threshold, the number of iFRZW you have is equal to the number of the FRZW in your staking position.

If your staking duration is below the threshold, the number of iFRZW you have will be linear decreased and adjusted.

If your staking position is ended, the number of iFRZW you have is 0.

For example, if the threshold is 20 weeks:&#x20;

* Your current fixed-term staking position has a duration of 25 weeks and 200 staked FRZW. Then the number of iFRZW you have is 200.&#x20;
* Your current fixed-term staking position has a duration of 10 weeks and 200 staked FRZW. Then the number of iFRZW you have equals 200 × (10 ÷ 20) = 100.&#x20;
* Your current fixed-term staking position has a duration of 2 weeks and 200 staked FRZW. Then the number of iFRZW you have equals 200 × (2 ÷ 20) = 20.&#x20;
* Your current fixed-term staking position has a duration of 2 weeks and 200 staked FRZW. But the position is ended. Then the number of iFRZW you have is 0.

|                  | Your staking duration is equal to or longer than the threshold | Your staking duration is shorter than the threshold                  |
| ---------------- | -------------------------------------------------------------- | -------------------------------------------------------------------- |
| **iFRZW Amount** | Equals your Locked FRZW Amount                                 | Equals your Locked FRZW Amount x (Your Staking Duration / Threshold) |

### How to check the number of iFRZW I have?

![](../../.gitbook/assets/image3.png)

You can check the number of iFRZW you have in the IFO page [here](https://FRZDEX.finance/ifo).

### **How to increase the number of iFRZW I have?**

You can increase the number of iFRZW you have by:

* Adding more FRZW to your fixed-term staking position in the FRZW syrup pool.
* Extend your fixed-term staking durations if your current durations is shorter than the threshold.

****![](../../.gitbook/assets/image2.png)****

You can preview the number of iFRZW generated from your staking position when adjusting or initializing the fixed-staking.

### What is the threshold for iFRZW calculations?

Between each IFOs, the kitchen will optimize the threshold based on the average staking duration of the fixed-term staking FRZW pool. The adjustment will be published on all social channels.

![](<../../.gitbook/assets/image (134).png>)

You can check the current threshold for iFRZW calculations by hovering or tapping the underlined iFRZW text in the FRZW syrup pool window.
