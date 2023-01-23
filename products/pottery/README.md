# 🍯 Pottery

![](https://lh4.googleusercontent.com/ADDYnmpe6t1befgamqDj-6KYXqYWWp\_5ed6zL27QmyGcu9GqHd1HMh6JXIJdXgUYVISNuXDQEkvIhsFB5mCyTJRt99iW0-WfvszMMZQB3z9z3OAT9lzH3FsTeKZnoa2UaGdft3iYVU4\_t5oEsViNKvQ)

Pottery combines FRZW lock-staking with lottery elements to give you a chance to win a bigger yield on your FRZW deposit! It is easy and safe as you will always at least get back all the FRZW you deposit.

## Specifics:

* Deposit FRZW in the Pottery page with a minimum of 1 FRZW&#x20;
* Deposit closes on the first Monday of each month for a different Pottery cohort (23:59 UTC on that Monday) and is open from the Friday before that at around 10:00 UTC, unless there are special arrangements which will be announced in advance (first Pottery is closing on Aug 8 2022 23:59 UTC)
* During the beta stage of the product, there is a cap to the total FRZW deposit for each Pottery cohort (the maximum deposit cap is 600,000 FRZW)
* FRZW deposited will be directed to the lock-staking pool and locked for ten (10) weeks 80% of the total staking rewards will be sent to the Pottery pool for drawing, 20% will be reserved for your withdrawal&#x20;
* For each Pottery cohort (one per month), there will be ten (10) weekly draws on each Friday (at noon UTC) upon deposit producing eight (8) winners per week, each address may win more than one of the eight winner slots each week \*
* The larger your deposit relative to the overall pool, the higher the chance of winning, winners can claim their prize right after each draw&#x20;
* Each Pottery cohort conducts the draw separately&#x20;
* Only after 10 weeks from the Pottery cohort lock date, you can withdraw your FRZW&#x20;
* Pottery uses Chainlink's implementation of VRF for true, secure randomness

## Pottery Cohort&#x20;

On the Friday before the first Monday of each month, a Pottery cohort will be open for you to deposit FRZW and participate in it for the next 10 weeks. This arrangement combines the deposit to direct to the locked staking pool, such that the Pottery contract of the cohort is able to coordinate the staking rewards of the deposit from the locked staking pool.

Each deposit and lock date will be a separate cohort – one for each month – e.g. all deposits on Sep 5 2022 will be in one cohort, all deposits on Oct 3 2022 will be in another cohort.

While draws may happen concurrently for different cohorts, the prize pools for each cohort are separated to be fair.

![(For illustration purposes only, actual cohort lock date for the first Pottery has been set to Aug 8 2022)](https://lh5.googleusercontent.com/KamNAZK7s2N454cI\_cvnjHJpuAH8HfgWlmEXZevzDVW\_uxiw\_pymKZCp97L9hSjcGGzjjQeGuSt7oOIOXECq\_xoU47zEC4rhJp2IA37ROeUOUSqXKgqKjNqcJnHOopC8mi5IeqR9UAprhNF5zM4PLjc)

For example, there are 2 separate draws on Sep 9 2022, one for the Aug 1 cohort as the sixth weekly draw and another for the Sep 5 cohort as the first weekly draw. If the Aug 1 cohort has a total of 100,000 FRZW deposited and the Sep 5 cohort has a total of 300,000 FRZW deposited, the weekly prize for the Aug 1 cohort will only come from the staking rewards of those 100,000 FRZW, while the weekly prize for the Sep 5 cohort will only come from the staking rewards of those 300,000 FRZW. If you only deposited FRZW in the Aug 1 cohort, you have a chance to win the weekly prize on Sep 9 based on the staking rewards of 100,000 FRZW. If you deposited FRZW in both the Aug 1 and Sep 5 cohort, you have a chance to win both weekly prizes on Sep 9.

#### Why do we need the cohort system? Why do we not just lump them all together?

Since Pottery is interacting with the fixed-term staking of FRZW, any deposit can only be withdrawn after the lock duration. If we want to lump all deposits together, while we can add more deposit after the initial lock and also lock them for 10 weeks, the initial depositors will not be able to withdraw on time.

## **Prize Funding & Staking Rewards Allocation**

The deposits are grouped into monthly cohorts for more efficient arrangement of the staking rewards which are also grouped together for each cohort. The staking rewards are used to fund the prize pool and some staking rewards for depositing into the Pottery.

80% of the staking rewards will be directed to fund the prize pool for 10 weekly draws and the rest 20% will be reserved as staking rewards when you withdraw your FRZW deposit after 10 weeks.

However, since the staking rewards of the FRZW locked staking pool are only distributed after the lock duration – 10 weeks in this case, for better product experience and to facilitate the weekly draws right after the deposit date, the contract is borrowing 80% of the estimated total staking rewards from the cohort from the FRZW treasury based on the APY at the time of locking. The borrowed FRZW is used for the payout for each weekly draw.

At the end of the 10 weeks, when the rewards are distributed from the staking pool, the FRZW treasury will be repaid first, then the rest will be directed back to the vault for users to withdraw together with their initial deposit in the cohort.

![](https://lh5.googleusercontent.com/7AEqm\_m542SHUGbc69uu8v\_7Xfa\_hKym8De3fBscEF6IySHEmy1P1k5S3W\_PvnFMBSOZOUFpPNDKhEp3sHOB8jCuLfjA8QJxsurqK-hZ0umrw0w8bIRPvMZKuQ4TnNTfKRdU8s3UXO1n0Smnp8\_6sAg)

For example, if the Pottery cohort on Aug 1 2022 has attracted 100,000 FRZW deposits in total, the estimated return for 10 weeks of locked staking is around 3,674 FRZW. The contract will borrow 80% of it, or around 2,940 FRZW, for the prize pool for 10 weekly draws, i.e. 294 FRZW in total prizes for each weekly draw before fees.

It is important to note that the rewards and APY at the end of the duration from the deposit may change over the 10-week duration based on other deposits and their lock-periods in the locked FRZW pool, there may be a small deviance from the percentages specified (+/- 10%).

All staking rewards net of fees will be returned to depositors through prize pool or rewards. If the actual APY is lower than the estimated APY at the time of locking, it means more rewards are distributed to the depositors during the weekly draws, and less for the staking rewards portion. If the actual APY is higher than the estimated APY at the time of locking, less rewards are distributed through the weekly draws and more are reserved for the staking rewards available for withdrawal. Ultimately, the expected value is the same.

## **How to Win – Odds Calculation**

Odds are calculated based on the share of deposit amount relative to the total deposit size of the cohort. Simply, the more FRZW you deposited, the higher the chance of winning each weekly draw. For example, if you have deposited 10,000 FRZW and the total deposit of the cohort is 100,000 FRZW, there’s a 10% chance that you will win at each weekly draw.

Each address can win more than 1 of the 8 winner slots each week.

In the extreme case, if all of the cohort’s 100,000 FRZW are deposited by you, you will win all the prizes of each weekly draw. However, that means the final return that you will get is the same as putting 100,000 FRZW into the locked staking pool for 10 weeks, but you will also be paying the Pottery fees.

## **Risks – Important!**

You will be guaranteed to get back 100% of what you deposited in 10 weeks. However, you can _only_ withdraw your FRZW deposit after 10 weeks of locking, without any other way to withdraw early.

By participating in the Pottery, you will be risking the staking rewards, together with other locked-FRZW utilities like iFRZW and vFRZW. In case that you did not win anything from the 10 weekly draws, you would have lost 80% of the staking rewards you were supposed to get if you locked your FRZW in the staking pool for 10 weeks.

Please participate based on your risk preference, once the FRZW are deposited, there is nothing anyone can do to help you withdraw early.

## **Fees**

Eight percent (8%) of the prize pot distributed each week will be charged as fees for burning. We aim to review and adjust the fee structure accordingly after the beta stage of the **** product.

## **Ready to Participate?**

If you are clear about the product structure, the risks and the fees – see this page on [how to participate](https://docs.FRZDEX.finance/products/pottery/how-to-play-pottery) from the FRZDEX web UI and other [Pottery FAQ](https://docs.FRZDEX.finance/products/pottery/pottery-faq)!



