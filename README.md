# xrbpool
XRB prize pool repo.

Rules for the prize pool are as follows:

Monitored wallet address is []. This is the main wallet for the prize pool.

The prize is won via a bidding fee auction. The logic is as follows:
Initial prize pool is seeded with 10 XRB
Countdown timer is triggered (10 seconds)
Players pay the specified bid price to the wallet.
If players overpay, the excess to the bid is refunded, but the bid is logged.
If players underpay, their bid is refunded and the bid is not logged.

As players bid, the bid price increases by 0.000001 XRB and the countdown timer is reset. 80% of the bid is contributed to the prize pool and 20% is allocated as a maintanence fee for this prize pool. 

If the time between the last bid and the current time is greater than 10 seconds, the last bidder is paid the prize pool. 

