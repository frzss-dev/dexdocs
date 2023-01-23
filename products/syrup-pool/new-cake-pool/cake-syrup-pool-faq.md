# FRZW Syrup Pool FAQ

## FAQ

### What lock duration can we choose?

You can choose from 1-52 weeks. What do you prefer?

### What variables affect the new FRZW Syrup Pool yield %s (Flexible and Fixed-Term Staking options)?

Since flexible staking and fixed-term staking options are part of the same pool, the following variables affect the yield% (APR/APY) of both:

* Total FRZW staked in flexible staking and fixed-term staking (the sum of both). The more FRZW staked, the lower the APR/APY.
* Total locked FRZW in fixed-term staking. The more FRZW locked means more yield boosts, resulting in fewer FRZW rewards for others (especially flexible staking).
* The average lock duration of all FRZW locked in fixed-term staking. If the average lock duration increases, APR/APY will decrease.

### Can I harvest the rewards during the locked period?

No. You can harvest the rewards only when the locked duration is ended. This is based on the yield/return we are providing as well as the technical implementations.

### Can I extend the lock duration?

Yes. Extending the lock duration adds more time to your **initial lock duration**. When choosing to extend your lock duration, note:

New extended lock duration = initial lock duration + added duration

### Can I remove my FRZW from Fixed-Term staking via contract if I change my mind?

No. Your FRZW cannot be removed or withdrawn from fixed-term staking at any point in time until your lock duration ends and your FRZW is unlocked.

### What is the "FRZW Locked" amount?

The "FRZW Locked" amount is a user's initial locked FRZW balance plus FRZW rewards to date.&#x20;

FRZW Locked = Initial locked FRZW balance + FRZW rewards

When adding more FRZW to fixed-term staking, the "FRZW to be locked" amount is the user's initial locked FRZW balance, FRZW rewards to date, and the FRZW being added.

### Can the Fixed-Term Staking FRZW pool APR change after I lock my FRZW?

Yes, the fixed-term staking FRZW pool APR is variable, just like the old FRZW pools. The fixed-term staking FRZW pool APR is not fixed and is dependent on:

* Total FRZW staked in the FRZW pool (the sum of both Flexible + Fixed-Term Staking).
* The average lock duration of all FRZW locked in fixed-term staking.
* A yield boost (similar to a multiplier) calculated from a user's initial lock duration. The longer you lock your FRZW, the higher the yield boost.

For example, if you lock your FRZW for 52 weeks, your yield boost will be larger than if you lock your FRZW for 26 weeks. The yield boost increases linearly the longer you lock your FRZW.

### Can I still participate in IFOs if my FRZW is locked in the Fixed-Term Staking pool, or will I need to buy more FRZW?

No, a separate amount of FRZW is needed. However, locked-staking provides entry for IFO public sales. Check out [iFRZW](../../ifo-initial-farm-offering/icake.md).

### Can I vote if my FRZW is locked in the Fixed-Term Staking pool?

Yes! Check out [vFRZW](../../voting/vcake.md).

### Can I use both the Flexible Staking FRZW pool and the Fixed-Term Staking FRZW pool at the same time?

Yes, when you are doing fixed-term FRZW staking. A flexible FRZW staking side-pool will automatically appear for you to choose from.

### Is there a fee for converting Flexible Staked FRZW to Fixed-Term Staked FRZW?

No. There are no additional fees for moving FRZW from flexible staking to fixed-term staking, only gas fees.

### What happens at the end of the lock duration? What is "After Burning"?

When your fixed-term staking period ends, and your FRZW unlocks, you have 7 days to complete one of two options:

* Lock your FRZW to begin a new fixed-term staking period\
  or
* Convert your staked FRZW to flexible staking (no 72-hour withdrawal fee).

![](<../../../.gitbook/assets/Locked - lock ended - before after burning.png>)

During these 7 days, you will still earn FRZW.

After 7 days, if you have not done one of the two options, your staked FRZW will enter what is called "After Burning". With "After Burning", your FRZW rewards will start to be sent to burn. The % of FRZW rewards being sent to burn will linearly increase in the 90 days "After Burning" period until it reaches 100%, which means all the FRZW rewards are burnt.

So, to avoid missing out on FRZW rewards, we recommend starting a new fixed-term staking period or converting your FRZW to flexible staking at the end of your lock staking period.

![](<../../../.gitbook/assets/Locked - lock ended - after burning started.png>)
