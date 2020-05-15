# Ch 5 Determination of Forward and Futures Prices 

## Investment Assets vs Consumption Assets

investment asset - asset that is held for investment purposes 

- stocks, bonds, gold, silver

consumption asset - asset that is held primarily for consumption 

- copper, crude oil, corn

Arbitrage arguments can be used to determine forward and futures prices for investment assets based on spot price and other market variables, but this cannot be done for consumption assets. 

## Short Selling

short selling - selling an asset that is not owned

- investor with short position must pay to the broker any income (dividends or interest) that would normally be received on the securities that have been shorted 
- broker then transfers the income to the account of the client from whom the securities have been borrowed 

margin account - consists of cash or marketable securities deposited by the investor with the broker to guarantee the investor will not walk away from the short position if the share price increases

- investor is required to maintain a margin account with the broker 
- does not represent a cost to the investor
-- interest is usually paid on the balance in margin accounts 

## Assumptions and Notation

Assume the following
1. Market participants are subject to no transaction costs 
2. Market participants are subject to same tax rate on all profits
3. Market participants can borrow money as same risk-free rate as they can lend 
4. Market participants take advantage of arbitrage opportunities as they occur

Notation

$T$ : Time until delivery date in a forward or futures contract (in years)
$S_0$ : Price of asset underlying the contract today
$F_0$ : Forward or futures price today
$r$ : Zero-coupon risk-free rate of interest per annum (continuous compounding) 

## Forward Price for an Investment Asset

- if forward price is too high, then investor can short the forward contract and borrow at the risk-free rate to lock in a profit
- if forward price is too low, then investor can long a forward contract and short the share to lock in a profit

#### A Generalization

Consider a forward contract on an investment asset with price $S_0$ that provides no income. 
The relationship between $F_0$ and $S_0$ (with time to maturity $T$ and risk-free rate $r$) is $$F_0 = S_0 e^{rT}$$ 
If $F_0 > S_0 e ^{rT}$ then arbitrageurs can buy the asset and short forward contracts.
If $F_0 < S_0 e^{rT}$ then arbitrageurs can short the asset and long forward contracts. 

Forward price is higher than spot price due to cost of financing the spot purchase of the asset during the life of the forward contract. 

#### What if Short Sales are not Possible?

- short sales are not possible for all investment assets 
- sometimes a fee is charged for borrowing assets

However, this does not matter, and the above does not require shorting the asset. 

Suppose underlying investment asset gives rise to no storage costs or income. 
If $F_0 > S_0 e^{rT}$ then the investor can:
1. Borrow $S_0$ dollars at interest rate $r$ for $T$ years
2. Buy 1 unit of the asset
3. Short a forward contract on 1 unit of the asset

At time $T$ the asset is sold for $F_0$, amount $S_0 e^{rT}$ is required to repay the loan, so the investor's profit is $F_0 - S_0 e^{rT}$. 

If $F_0 < S_0 e^{rT}$ then the investor who owns the asset can:
1. Sell the asset for $S_0$
2. Invest the proceeds at interest rate $r$ for $T$ years
3. Take a long position in a forward contract on 1 unit of the asset 

At time $T$ the cash invested has grown to $S_0 e^{rT}$, the asset is repurchased for $F_0$, so the investor's profit is $S_0 e^{rT} - F_0$. 

## Known Income

#### A Generalization

When an investment asset will provide income with a present value of $I$ during the life of a forward contract, then $$F_0 = (S_0 - I) e^{rT}$$

If $F_0 > (S_0 - I) e^{rT}$ then an arbitrageur can lock in a profit by buying the asset and shorting a forward contract on the asset. 

If $F_0 < (S_0 - I) e^{rT}$ then an arbitrageur can lock in a profit by shorting the asset and taking a long position in a forward contract. 

If short sales are not possible, then investors who own the asset will find it profitable to sell the asset and enter into long forward contracts. 

## Known Yield

Consider situations where the asset underlying the forward contract provides a known yield rather than a known cash income. This means the income is known when expressed as a percentage of the asset's price at the time the income is paid. 

Define $q$ as the average yield per annum on an asset during the life of a forward contract with continuous compounding. $$F_0 = S_0 e^{(r-q)T}$$

## Valuing Forward Contracts

- value of a forward contract at the time it is first entered into is close to zero
-- may be positive or negative later 
- important to value the contract each day (marking to market) 

Let $K$ be delivery price for contract, delivery date in $T$ years, and $r$ risk-free rate. 
Then $F_0$ is the forward price applicable if contract is negotiated today.
Let $f$ be value of forward contract today. 

At beginning of contract life, $K = F_0$ and $f = 0$. 
As time passes, $K$ stays the same, but forward price changes, so $f$ changes. 

Generally, $$f = (F_0 - K) e^{-rT}$$

Value of forward contract on an investment asset that provides no income $$f = S_0 - K e^{-rT}$$
Value of forward contract on an investment asset that provides a known income with present value $I$ $$f = S_0 - I - K e^{-rT}$$
Value of forward contract on an investment asset that provides a known yield at rate $q$ $$f = S_0 e^{-qT} - K e^{-rT}$$

Futures vs Forwards

- when price changes, the gain or loss is equal to contract price multiplied by size of position
- when futures price changes, the gain or loss is realized immediately due to daily settlement
- when forward price changes, the gain or loss is the present value of the change 

## Are Forward Prices and Futures Prices Equal?

- when short-term risk-free interest rate is constant, the forward price is the same as the futures price
- when interest rates vary unpredictably, forward and futures prices are no longer the same 

Consider situation where price of underlying asset $S$ is strongly positively correlated with interest rates. 

When $S$ increases:
- investors with long futures positions can make immediate gains because of daily settlement
- positive correlation means interest rates have also increased
- the gain will be invested at a higher interest rate 

When $S$ decreases: 
- investor will incur an immediate loss
- loss will be financed at lower interest rate 

An investor holding a forward contract is not affected in this way by interest rate movements. 
Thus a long futures contract is more attractive than a forward contract. 

$\Rightarrow$ When $S$ is strongly positively correlated with interest rates, futures price $>$ forward price 
$\Rightarrow$ When $S$ is strongly negatively correlated with interest rates, futures price $<$ forward price 

---
There are other factors that cause forward and futures prices to differ.
- taxes
- transaction costs
- margin requirements
- default risk 
- differences in liquidity 

It is generally reasonable to assume that forward and future prices are the same. 

## Futures Prices of Stock Indices

quanto - derivative where the underlying asset is measured in one currency and the payoff is in another currency
- example: CME futures contract on the Nikkei 225 Index 
-- contract is measured in dollars but the underlying asset is measured in yen 

The following equation applies only when the value of a portfolio of assets can be traded (does not apply to quantos).

$$F_0 = S_0 e^{(r-q)T}$$

#### Index Arbitrage

If $F_0 > S_0 e^{(r-q)T}$ then profit can be made by buying the stocks underlying the index at the spot price and shorting the futures contracts. 

If $F_0 < S_0 e^{(r-q)T}$ then profit can be made by shorting the stocks underlying the index and taking a long position in the futures contracts. 

The above strategies are *index arbitrage*. 

- sometimes accomplished by trading a small representative sample of stocks whose movements closely mirror those of the index 

## Forward and Futures Contracts on Currencies

Consider forward and futures foreign currency contracts from the perspective of a US investor. 
The underlying asset is one unit of the foreign currency.

$S_0$ : current spot price in US dollars of one unit of the foreign currency
$F_0$ : forward or futures price in US dollars of one unit of the foreign currency

A foreign currency has the property that the holder of the currency can earn interest at the risk-free interest rate in the foreign country. 

Define $r_f$ as value of foreign risk-free rate when money is invested for time $T$. 
Define $r$ as risk-free rate when money is invested in US dollars for time $T$. 

$$F_0 = S_0 e^{(r-r_f)T}$$

---
Derivation of the previous equation.

There are two ways to convert 1000 units of foreign currency to dollars at time $T$. 

1. Invest it for $T$ years at rate $r_f$ and enter into a forward contract to sell the proceeds for dollars at time $T$. 
$$\Rightarrow 1000 e^{r_f T} F_0$$

2. Exchange the foreign currency for dollars in the spot market and invest the proceeds for $T$ years at rate $r$. 
$$\Rightarrow 1000 S_0 e^{rT}$$

These must be equal in the absence of arbitrage opportunities.
$$1000 e^{r_f T} F_0 = 1000 S_0 e^{rT}$$ which gives $$F_0 = S_0 e^{(r-r_f)T}$$

## Futures on Commodities

#### Income and Storage Costs

In the absence of storage costs and income, the forward price of a commodity that is an investment asset is given by $$F_0 = S_0 e^{rT}$$

Storage costs can be treated as negative income. 
Let $U$ be the present value of all storage costs, net of income, during life of forward contract. 
$$F_0 = (S_0 + U) e^{rT}$$

Treat storage costs that are proportional to commodity price as negative yield.
$$F_0 = S_0 e^{(r+u)T}$$ where $u$ denotes storage cost per annum as a proportion of spot price net of any yield earned on the asset. 

#### Consumption Commodities

- usually provide no income 
- can be subject to significant storage costs 

Suppose $F_0 > (S_0 + U) e^{rT}$ then an arbitrageur can implement the following strategy.
1. Borrow an amount $S_0 + U$ at the risk-free rate and purchase one unit of the commodity and to pay storage costs.
2. Short a futures contract on one unit of the commodity.

Suppose $F_0 < (S_0 + U) e^{rT}$ then an arbitrageur can implement the following strategy. 
1. Sell the commodity, save the storage costs, and invest proceeds at risk-free rate. 
2. Take a long position in a futures contract. 

The above argument is true for **investment assets** which are held solely for investment. 
The argument cannot be used for **consumption assets**. 

- consumption commodities are usually owned in order to use in some way 
- owners are reluctant to sell the commodity in the spot market and buy futures contracts because these contracts cannot be consumed 

There is no arbitrage argument that prevents $F_0 < (S_0 + U) e^{rT}$ from holding. 
The only possible assertion for commodity assets is $$F_0 \le (S_0 + U) e^{rT}$$ or equivalently for storage costs expressed as a proportion $u$ of the spot price $$F_0 \le S_0 e^{(r+u)T}$$

#### Convenience Yields

convenience yield - benefits from holding the physical asset 

If dollar amount of storage costs has present value $U$ then the convenience yield $y$ is defined so $$F_0 e^{yT} = (S_0 + U) e^{rT}$$

If the storage costs per unit are a constant proportion $u$ of the spot price then $y$ is defined so $$F_0 e^{yT} = S_0 e^{(r+u)T}$$ $$F_0 = S_0 e^{(r+u-y)T}$$

For investment assets the convenience yield must be zero to prevent arbitrage opportunities. 

The convenience yield reflects market expectations concerning futures availability.
- greater possibility of shortages means higher convenience yield
- low chance of shortages means low convenience yield 

## The Cost of Carry

cost of carry - storage cost plus interest paid to finance asset less the income earned on asset

For a non-dividend-paying stock the cost of carry is $r$ (no storage costs and no income earned)
For a stock index the cost of carry is $r-q$ (income is earned at rate $q$ on the asset)
For a currency the cost of carry is $r-r_f$
For a commodity that provides income at rate $q$ and requires storage costs at rate $u$ the cost of carry is $r-q+u$

Let the cost of carry be $c$.
For an investment asset the futures price is $$F_0 = S_0 e^{cT}$$ For a consumption asset it is $$F_0 = S_0 e^{(c-y)T}$$ where $y$ is the convenience yield. 

## Delivery Options

- forward contract specifies that delivery is to take place on a particular day
- futures contract allows party with short position to choose to deliver at any time during a certain period 

Should maturity of futures contract be at the beginning, middle, or end of the delivery period?

If futures price is an increasing function of time to maturity then $c > y$
- benefits from holding asset are less than risk-free rate
- optimal to deliver as early as possible
- futures prices should be based on delivery taking place at beginning of delivery period

If futures price is decreasing as time to maturity increases then $c < y$
- benefits from holding asset are greater than risk-free rate
- optimal to deliver as late as possible
- futures prices should be based on delivery at end of delivery period 

## Futures Prices and Expected Future Spot Prices

expected spot price - market's average opinion on what spot price of an asset will be 

Futures prices converge to spot price at maturity.
If futures price > expected spot price, then traders with short positions gain. 
If futures price < expected spot price, then traders with long positions gain. 

#### Keynes and Hicks

If hedgers tend to hold short positions and speculators tend to hold long positions, the futures price of an asset will be below the expected spot price. 

- because speculators require compensation for the risks they are bearing
-- will trade only if they can expect to make money on average
- hedgers will lose money on average
-- prepared to accept this because the futures contract reduces their risks

If hedgers tend to hold long positions while speculators hold short positions, the futures price will be above the expected spot price, for similar reasons. 

#### Risk and Return

- the higher the risk, the higher the expected return demanded by an investor

Two types of risk in the economy
1. Systematic 
2. Nonsystematic

Nonsystematic Risk 
- should not be important to an investor 
- can be completely eliminated by holding a well-diversified portfolio 
- investor should not require higher expected return for bearing nonsystematic risk

Systematic Risk
- cannot be diversified away 
- arises from correlation between returns from investment and returns from whole stock market
- investor requires higher expected return than the risk-free rate for bearing positive amounts of systematic risk
- investor is prepared to accept a lower expected return than the risk-free rate when the systematic risk in an investment is negative 

#### The Risk in a Futures Position

The futures price is an unbiased estimate of the expected future spot price when the return from the underlying asset is uncorrelated with the stock market. 

| *Underlying asset* | *Expected return vs risk-free rate* | *Futures price vs expected future spot price* | 
| :--------- | :------: | :--------: |
| No systematic risk | $k=r$ | $F_0 = E(S_T)$
| Positive systematic risk | $k > r$ | $F_0 < E(S_T)$ |  
| Negative systematic risk | $k < r$ | $F_0 > E(S_T)$ | 

#### Normal Backwardation and Contango

normal backwardation - futures price is below the expected future spot price
contago - futures price is above the expected future spot price 
