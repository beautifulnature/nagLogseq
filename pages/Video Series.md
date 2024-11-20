- https://zerodha.com/varsity/chapter/introduction-to-options/
- [1. Introduction to Options](https://www.youtube.com/watch?v=-mO0YOTcCiQ)
  collapsed:: true
	- Options are derivative contracts
	- Call options
	- Put options
- [Option Jargons – Varsity by Zerodha](https://zerodha.com/varsity/chapter/option-jargons/)
  collapsed:: true
	- SBIN OCT 460 CE
	  collapsed:: true
		- underlying = SBIN (State Bank of India)
		- Expiry Date = OCT is  (last Thursday of October)
		- Strike Price = 460
		- Option Type = Call (CE is Call Option European)
		- Premium = 17.75
		- Lot size = 1500
	- Ask yourself
	  collapsed:: true
		- risk?
		- worst case scenario?
		- break even point?
		- maximum gain?
	- summary
	  collapsed:: true
		- it makes sense to buy a call option only when one anticipate an increase in the price of an asset
		- the strike price is the anchor price at which both the option buyer and option writer enter into an agrement
		- the underlying price is simply the spot price of the asset
		- exercising of an option contract is the act of claiming your right to buy the options contract at the end of the expiry
		- similar to futures contract, options contract also have an expiry. options contracts expire on the last Thursday of every month
		- options contracts have different expiries - the current month, mid month, and far month contracts
		- the option buyer benefits only if the price of the asset increases higher than the strike price
		- premiums are not fixed, in fact they vary based on several factors that act upon it
		- options are cash settled in India.
- [3. Long Call Payoff and Short Call Trade - YouTube](https://www.youtube.com/watch?v=jEHgjGrHFNU)
  collapsed:: true
	- stock price increase
	  collapsed:: true
		- if price goes to 500, profit is 40.
		- Realised profit = 40
		- Premium paid = 17.50
		- Net profit = 22.50 (40 - 17.50)
		- Makes money when Market price increases
	- stock price remains same
	  collapsed:: true
		- Premium paid = 17.50
		- Realised Loss = 17.50
		- Let go off right to buy option
		- Loses money when market stays flat
	- stock price decrease
	  collapsed:: true
		- Premium paid = 17.50
		- Let go off right to buy option
		- Loses money when market falls
	- Buy Call Option when you are bullish on the underlying until expiry
	- example:
	  collapsed:: true
		- Long Call pay off / SBI
			- Option Type - Call Option
			  Position - Buy
			  Strike - 460
			  Premium Paid - 17.5
			  Expiry - 30 days
		- |Possible expiry|Premium paid|P&L|
		  |285|-17.5|-17.5|
		  |302.5|-17.5|-17.5|
		  |320|-17.5|-17.5|
		  |337.5|-17.5|-17.5|
		  |355|-17.5|-17.5|
		  |372.5|-17.5|-17.5|
		  |390|-17.5|-17.5|
		  |407.5|-17.5|-17.5|
		  |425|-17.5|-17.5|
		  |442.5|-17.5|-17.5|
		  |460|-17.5|-17.5|
		  |477.5|-17.5|0|
		  |495|-17.5|17.5|
		  |512.5|-17.5|35|
		  |530|-17.5|52.5|
		  |547.5|-17.5|70|
		  |565|-17.5|87.5|
		  |582.5|-17.5|105|
		  |600|-17.5|122.5|
		  |617.5|-17.5|140|
		  |635|-17.5|157.5|
		  |652.5|-17.5|175|
		- TODO make a P&L chart for buyer and seller
		  :LOGBOOK:
		  CLOCK: [2024-11-20 Wed 16:06:48]--[2024-11-20 Wed 16:06:49] =>  00:00:01
		  :END:
		- Max Loss (Buyer) = Max Profit (Seller)
	- summary
	  collapsed:: true
		- It makes sense to be a buyer of a call option when you expect the underlying price to increase
		- if the underlying price remains flat or goes down then the buyer of the call option loses money
		- the money the buyer of the call option would lose is equivalent to the premium (agreement fees) the buyer pays to the seller/writer of the call option
		- intrinsic value (IV) of a call option is a non negative number
		- IV = Max [(0, (spot price - strike price)]
		- the maximum loss the buyer of a call option experiences is to the extent of the premium paid. the loss is experienced as long as the spot price is below the strike price
		- the call option buyer has the potential to make unlimited profits provided the spot price moves higher than the strike price.
		- though the call option is supposed to make a profit when the spot price moves above strike price, the call option buyer first needs to recover the premium he has paid
		- the point at which the call option buyer completely recovers the premium he has paid is called the breakeven point
		- the call option buyer truly starts making a profit only beyond the break even point (which naturally is above the strike price)
- [4. Put Buy and Put Sell](https://www.youtube.com/watch?v=48VEFNn2gbo)
  collapsed:: true
	- RELIANCE OCT 2560 PE
	- underlying = RELIANCE
	  expiry = OCT (last Thursday of October)
	  strike price = 2560
	  PE = Put Option European
	  premium = 72.6
	  Lot Size = 250
	- stock price increase
	  collapsed:: true
		- RELIANCE stock price on expiry date = 2800
		- forfeit right to sell and let go the premium paid
		- Premium paid = 72.50
		- Realised Loss = 72.50
	- stock price remains flat
	  collapsed:: true
		- RELIANCE stock price on expiry date = 2560
		- forfeit right to sell and let go the premium paid
		- Premium paid = 72.50
		- Realised Loss = 72.50
	- stock price decrease
	  collapsed:: true
		- RELIANCE stock price on expiry = 2400
		- Realised Profit = 160 (2560 - 2400)
		- Premium paid = 72.50
		- Net profit = 87.50 (160 - 72.50)
		- Total Profit = 21875 (87.50 X 250)
	- Put option buyer makes money when market falls
	- Put option buyer loses money when market stays flat or when market rises
	- summary
		- buy a put option when you are bearish about the prospects of the underlying. in other words, a put option buyer is profitable only when the underlying declines in value
		- the intrinsic value calculation of a put option is slightly different when compared to the intrinsic value calculation of a call option
		- IV (Put option) = Strike Price - Spot Price
		- The P&L of a Put option buyer can be calculated as P&L = [Max(0, Strike Price - Spot Price)] - Premium paid
		- The break even point for the put option buyer is calculated as Strike - Premium Paid