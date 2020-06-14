# Ch 2 Mechanics of Futures Markets

- vast majority of futures contracts do not lead to delivery
-- traders close out positions prior to delivery period specified in the contract
- possibility of final delivery ties the futures price to the spot price

## Specification of a Futures Contract

- exchange must specify the following in the contract
-- asset
-- contract size 
-- where and when delivery can be made

- when party with short position is ready to deliver it files a *notice of intention to deliver*
-- indicates grade of asset delivered and delivery location

#### The Asset

- when the asset is a commodity, there may be variation in the quality 
-- exchange must stipulate the grade(s) that are acceptable 
-- price may depend on the grade, with adjustments established by the exchange 

#### The Contract Size

- contract size specifies the amount of the asset that has to be delivered under one contract
-- if too large: investors wishing to hedge small exposures or take small speculative positions cannot do so
-- if too small: trading may be expensive due to transaction costs
- exchanges have introduced "mini" contracts to attract smaller investors

#### Delivery Arrangements

- exchange must specify where delivery will be made
-- price received by party with short position may be adjusted according to location chosen by that party, when alternative delivery locations are specified 
-- price tends to be higher for delivery locations far from the main source of the commodity 

#### Delivery Months

- exchange must specify precise period during the month when delivery can be made 
-- for many futures contracts the delivery period is the whole month
- contracts trade for closest delivery month and a number of subsequent delivery months
-- exchange specifies when trading for a particular month's contract begins and ends 
-- trading usually ends a few days before the last day on which delivery can be made 

#### Price Quotes

- exchange defines how prices will be quoted 
-- example: dollars and cents, or dollars and thirty-seconds of a dollar 

#### Price Limits and Position Limits

- exchange specifies daily price movement limits

limit down - price moves down from previous day's close by amount equal to daily price limit
limit up - price moves up from previous day's close by amount equal to daily price limit
limit move - move in either direction equal to daily price limit

- trading ceases for the day once contract is limit up or limit down
-- in some cases, the exchange can step in and change the limits 

- purpose of daily price limits is to prevent large price movements due to speculative excesses
-- however, limits can become an artificial barrier to trading when price of underlying is changing rapidly

- position limits are max number of contracts that a speculator may hold 
-- purpose is to prevent speculators from exercising undue influence on the market

## Converge of Futures Price to Spot Price

- as delivery period approaches, futures price converges to spot price of underlying 
-- when delivery period is reached, futures price equals spot price (roughly)
-- if not, arbitrage opportunities exist, causing prices to converge

## Operation of Margin Accounts

- a key role of the exchange is to organize trading to avoid contract defaults 

#### Daily Settlement

initial margin - amount that must be deposited at the time the contract is entered into 

- at EOD the margin account is adjusted to reflect investor's gain/loss 
-- known as *daily settlement* or *marking to market*

- investor can withdraw any balance in margin account excess of initial margin 

maintenance margin - ensures balance in margin account never becomes negative

- lower than initial margin
- if balance in margin account falls below maintenance margin, investor receives a **margin call**
-- investor must fund margin account to the initial margin level by end of next day 
-- extra funds known as *variation margin*
-- if investor fails to do so, broker closes out the position 

#### Further Details

- most brokers pay investors interest on the balance in a margin account
- investor can deposit securities with the broker to satisfy initial margin requirements
-- but not for margin calls

- minimum margin levels set by exchange clearing house 
-- individual brokers may require greater margins from clients than those set by clearing house
-- minimum margin levels determined by variability of price of underlying 
-- higher variability leads to higher margin levels 
-- maintenance margin is usually ~75% of initial margin 

- margin requirements may depend on trader objectives
-- hedger may have lower margin requirements than a speculator due to less risk of default

day trade - trader announces to broker an intent to close out position in the same day
spread transaction - trader simultaneously buys a contract on an asset for one maturity month and sells a contact on the same asset for another maturity month 

- day trades and spread transactions give rise to lower margin requirements than do hedge transactions 

- short futures positions have same margin requirements as long futures positions
-- not true of spot markets, where taking a short position involves selling an asset that is not owned 

#### The Clearing House and its Members

clearing house - acts as intermediary in futures transactions

- purpose is to keep track of all transactions that take place during a day to calculate net position of each of its members

- initial margin determination is based on number of contracts outstanding on a net basis
-- short positions are offset against long positions 

- clearing house members required to contribute to a *guaranty fund*
-- used by clearing house in the event a member fails to provide variation margin and there are losses when the member's positions are closed out 

#### Credit Risk

- in Oct 1987 the S&P 500 index declined sharply and traders with long positions in S&P 500 futures had negative margin balances
-- those who did not meet margin calls were closed out but owed brokers money
-- some did not pay so brokers went bankrupt
-- however, clearing houses had sufficient funds to ensure everyone who had a short futures position got paid 

## OTC Markets

- credit risk is a key feature of OTC derivatives markets

#### Central Counterparties

- there are clearing houses for OTC transactions much like exchange clearing houses
-- members required to provide initial margin, daily variation margin, and contribute to guaranty fund

- clearing house takes on credit risk of both parties 
- if OTC market participant is not a member of a CCP, it can arrange to clear its trade via a CCP member

#### Bilateral Clearing

- OTC transactions not cleared via CCP are cleared bilaterally
-- two parties enter into a master agreement covering all their trades
-- often includes annex requiring one or both parties to provide collateral 

#### Futures Trades vs OTC Trades

- initial margin when provided as cash usually earns interest
-- daily variation margin does not earn interest 
- transactions in OTC market are not settled daily so daily variation margin provided by members does earn interest when provided as cash 

- securities can be used to satisfy margin or collateral requirements
-- market value of securities is reduced to determine their value for margin purposes
-- reduction is known as **haircut**

## Market Quotes

settlement price - price used for calculating daily gains/losses and margin requirements 
- usually the price at which the contract traded immediately before the end of a day's trading session

trading volume - number of contracts traded in a day
open interest - number of contracts outstanding

normal market - futures prices increase with maturity
inverted market - futures prices decline with maturity 

## Delivery

- very few futures contracts lead to delivery of the underlying 
- period during which delivery can be made is defined by the exchange 
- decision on when to deliver is made by the party with the short position 
-- notice of intention to deliver states how many contracts will be delivered and where delivery will be made and what grade will be delivered
- exchange chooses a party with a long position to accept delivery
-- usually the party with the oldest outstanding long position 
- parties with long positions must accept delivery notices
-- may find another party with an outstanding long position to transfer the notice to 
- party taking delivery is responsible for all warehousing costs 

Three critical days for a contract
1. *first notice day* - first day on which a notice of intention to deliver can be submitted to the exchange
2. *last notice day* - last day on which a notice of intention to deliver can be submitted to the exchange
3. *last trading day* - usually a few days before the last notice day 

- investor should close long positions prior to first notice day to avoid risk of having to take delivery 

#### Cash Settlement

- some futures are settled in cash because it is inconvenient/impossible to deliver the underlying asset 
- outstanding contracts are declared closed on a predetermined day
-- final settlement price equals spot price of the underlying asset at either open or close of trading on that day 

## Types of Traders and Types of Orders

Two main types of traders
1. *futures commission merchants* (FCMs)
-- following instructions of their clients and charge a commission for doing so 
2. *locals*
-- trading on their own account

scalpers - speculators watching for short-term trends and attempting to profit from small changes in the contract price; hold positions for only a few minutes 

day traders - hold positions for less than one trading day 

position traders - hold positions for much longer periods of time 

#### Orders

market order - request trade be carried out immediately at best price available in the market

limit order - specifies a particular price
- order can be executed only at this price or at one more favorable to the investor 
- no guarantee that order is executed at all 

stop order (stop-loss order) - specifies a particular price 
- order is executed at best available price one a bid or offer is made at the particular price or a less favorable price 
- a stop order becomes a market order once the specified price has been reached 
- purpose is to close out a position if unfavorable price movements take place 
-- limits the loss that can be incurred

stop-limit order - combination of a stop order and a limit order
- becomes a limit order as soon as a bid or offer is made at a price equal to or less favorable than the stop price 
- must specify both the stop price and the limit price 

market-if-touched (MIT) order - executed at best available price after a trade occurs at a specified price or at a more favorable price than the specified price 
- becomes a market order once the specified price has been reached 
- also known as a *board order* 
- designed to ensure profits are taken if sufficiently favorable price movements occur

discretionary order (market-not-held order) - traded as a market order except that execution may be delayed at the broker's discretion in an attempt to get a better price 

time-of-day order - specifies a particular period of time during the day when the order can be executed 

open order (good-til-canceled order) - in effect until executed or until end of trading in the particular contract

fill-or-kill order - must be executed immediately or not at all 

## Regulation

Futures markets in the US are regulated by Commodity Futures Trading Commission (CFTC)
- responsible for ensuring prices are communicated to the public 
- futures traders must report outstanding positions if above certain levels 
- licenses individuals who offer services to the public in futures trading 
- deals with complaints brought by public and ensures disciplinary action is taken when appropriate
- has authority to force exchanges to take disciplinary action against members 

National Futures Association (NFA) - organization of individuals who participate in the futures industry 
- objective is to prevent fraud and to ensure market operates in best interests of the public 
- authorized to monitor trading and take disciplinary action when appropriate 
- has efficient system for arbitrating disputes between individuals and its members 

Dodd-Frank act expanded role of CFTC
- now responsible for rules requiring that standard OTC derivates be traded on swap execution facilities and cleared through central counterparties

#### Trading Irregularities

- futures markets usually operate efficiently and in public interest 
- one type of irregularity is when investors *corner the market* 
-- investors take a huge long futures position and try to exercise control over supply of underlying commodity 
-- as maturity approaches, investors do not close out positions, so number of outstanding futures contracts may exceed the amount of the commodity available for delivery 
-- holders of short positions have difficulty delivering and try to close their positions
-- results in large rise in both futures and spot prices 
-- regulators deal with this by increasing margin requirements or imposing stricter position limits or prohibiting trades that increase a speculator's open position or requiring market participants to close out their positions 

- other irregularities 
-- overcharging customers
-- not paying customers the full proceeds of sales
-- traders using knowledge of customer orders to first trade for themselves (**front running**)

## Accounting and Tax

#### Accounting

- if contract does not qualify has a hedge
-- changes in market value of futures contract are recognized when they occur
- if contract does qualify as a hedge
-- gains/losses are recognized in the same period in which gains/losses from item being hedged are recognized (*hedge accounting*)

#### Tax

- gains/losses are either capital gains/losses or part of ordinary income
- for corporate taxpayers, capital gains are taxed at the same rate as ordinary income
-- ability to deduct losses is restricted 
- positions in futures contracts treated as if closed out on last day of tax year 
- gains/losses from hedging transactions are treated as ordinary income 

## Forward vs Futures Contracts

- both are agreements to buy or sell an asset for a certain price at a certain future time
-- forwards are traded in OTC markets with no standard contract size or standard delivery arrangements
-- futures have standardized contracts traded on an exchange 

#### Profits from Forward and Futures Contracts 

- with forwards, the whole gain or loss is realized at the end of life of the contract
- with futures, the gain or loss is realized day by day because of daily settlement procedures

#### Comparison 

| Forward | Futures |
| :------- | :------ |
| Private contract between two parties | Exchange-traded |  
| Not standardized | Standardized contract |  
| Usually one specified delivery date | Range of delivery dates |
| Settled at end of contract | Settled daily |  
| Delivery usually takes place | Usually closed prior to maturity |  
| Some credit risk | Virtually no credit risk |  
