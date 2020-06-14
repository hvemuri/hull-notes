# Ch 3 Hedging Strategies Using Futures

perfect hedge - a hedge that completely eliminates risk 
hedge-and-forget strategy - no attempt is made to adjust the hedge once it has been put into place

## Basic Principles

- objective is to take a position that neutralizes the risk as far as possible

#### Short Hedges

short hedge - involves a short position in a futures contract 
- appropriate when hedger already owns an asset and expects to sell it in the future 
- appropriate when asset is now owned now but will be owned in the future 

#### Long Hedges

long hedge - involves a long position in a futures contract 
- appropriate when hedger knows it will have to purchase an asset in the future 
- typically more advantageous than buying in the spot market immediately due to avoiding interest and storage costs 

## Arguments For and Against Hedging

#### Hedging and Shareholders

- one argument is that shareholders can hedge for themselves rather than the company doing it for them
-- argument assumes shareholders have as much info as company mgmt about risks faced by company
-- argument ignores commissions and other transaction costs 
- hedging is likely less expensive on a larger scale 
--- size of futures contracts makes hedging by individuals impossible in many situations
- shareholders can diversity risk more easily than a corporation can 
-- shareholder with a well-diversified portfolio may be immune to risks faced by a company

#### Hedging and Competitors

- if hedging is not the norm in a certain industry, it may not make sense for one particular company to hedge 
-- competitive pressures may cause prices to reflect material costs, interest rates, exchange rates, etc 
-- a company that hedges would have fluctuating profit margins whereas companies that do not hedge could expect constant profit margins

#### Hedging Can Lead to a Worse Outcome

- hedging reduces risk for the company
- if the price moves favorably, then the hedge can result in a loss that offsets the favorable price movement 
- only real solution is to ensure all executives understand the nature of hedging before employing a hedging strategy 
-- hedging strategies should be set by board of directors and communicated to company mgmt and shareholders 

## Basis Risk

Complications to hedging
1. The asset whose price is to be hedged may not be exactly the same as the asset underlying the futures contract
2. The hedger may be uncertain as to the exact date when the asset will be bought or sold
3. The hedge may require the futures contract to be closed out before its delivery month

The above problems give rise to **basis risk**

#### The Basis

Basis = Spot price of asset to be hedged - Futures price of contract used 

#### Choice of Contract

One key factor affecting basis risk is the choice of futures contract to be used for hedging, which has two components:
1. The choice of the asset underlying the futures contract
2. The choice of the delivery month

- choice of delivery month is influenced by many factors
-- long hedger runs risk of having to take delivery of the physical asset 
-- futures prices can be erratic during delivery month

- basis risk increases as time difference between hedge expiration and delivery month increases
-- choose a delivery month as close as possible to but later than the hedge expiration 

- liquidity is greatest in short-maturity futures contracts
-- hedger may be inclined to use short-maturity contracts and roll them forward 

## Cross Hedging

cross hedging - when asset underlying futures contract is different from the asset whose price is being hedged

hedge ratio - ratio of size of position in futures contract to size of exposure

- hedger should choose a value that minimizes the variance of the value of the hedged position 

#### Calculating the Minimum Variance Hedge Ratio

$\Delta S$ : Change in spot price, $S$, during a period of time equal to the life of the hedge
$\Delta F$ : Change in futures price, $F$, during a period of time equal to the life of the hedge 

The minimum variance hedge ratio $h^*$ is the slope of the best-fit line from a linear regression of $\Delta S$ against $\Delta F$. 
$$h^* = \rho \frac{\sigma_S}{\sigma_F}$$ where $\sigma_S$ is the standard deviation of $\Delta S$, $\sigma_F$ is the standard deviation of $\Delta F$, and $\rho$ is the coefficient of correlation between the two. 

The *hedge effectiveness* is the proportion of the variance eliminated by hedging, given by $R^2$ ($\rho^2$). 

- the parameters are usually estimated from historical data on $\Delta S$ and $\Delta F$. 

#### Optimal Number of Contracts

$Q_A$ : Size of position being hedged 
$Q_F$ : Size of one futures contract
$N^*$ : Optimal number of futures contracts for hedging

The number of futures contracts is given by 
$$N^* = \frac{h^* Q_A}{Q_F}$$ 

#### Tailing the Hedge

- the above analysis is based on forward contracts for hedging
- with futures contracts, there is daily settlement and series of one-day hedges
-- calculate correlation between percentage one-day changes in the futures and spot prices

If $S$ and $F$ are current spot and futures prices, the standard deviations of one-day price changes are $S\hat{\sigma}_S$ and $F\hat{\sigma}_F$ and the one-day hedge ratio is 
$$\hat{\rho} \frac{S\hat{\sigma}_S}{F\hat{\sigma}_F}$$ The number of contracts needed to hedge over the next day is 
$$N^* = \hat{\rho} \frac{S\hat{\sigma}_S Q_A}{F\hat{\sigma}_F Q_F}$$ Which can be written as 
$$N^* = \hat{h} \frac{V_A}{V_F}$$ where $V_A$ is the dollar value of the position being hedged, $V_F$ is the dollar value of one futures contract, and $\hat{h}$ is defined similarly to $h^*$ as 
$$\hat{h} = \hat{\rho} \frac{\hat{\sigma}_S}{\hat{\sigma}_F}$$ The result suggests that we should change the futures position every day to reflect the latest values of $V_A$ and $V_F$, but in practice the day-to-day changes are very small and are ignored. 

## Stock Index Futures

stock index - tracks changes in the value of a hypothetical portfolio of stocks 

#### Stock Indices

- *Dow Jones Industrial Average* - based on a portfolio of 30 blue-chip stocks in the US
-- weights proportional to stock prices
- *S&P 500 Index* - based on a portfolio of 500 different stocks 
-- weights proportional to market capitalizations 
- *Nasdaq-100* - based on 100 stocks 

#### Hedging an Equity Portfolio

Stock index futures can be used to hedge a well-diversified equity portfolio

$V_A$ : Current value of the portfolio
$V_F$ : Current value of one futures contract (futures price times contract size)

If the portfolio mirrors the index then the optimal hedge ratio is 1.0, so the number of futures contracts that should be shorted is $$N^* = \frac{V_A}{V_F}$$

If the portfolio does not mirror the index then use CAPM. The parameter $\beta$ is the slope of the best-fit line obtained when excess return on portfolio at risk-free rate is regressed against excess return of the index at risk-free rate. 

$\beta = 1.0$ means portfolio tends to mirror return on index
$\beta = 2.0$ means excess return on portfolio tends to be twice as great as excess return on index

A portfolio with $\beta = 2.0$ is twice as sensitive to movements in the index as a portfolio with $\beta = 1.0$, so need twice as many contracts to hedge the portfolio. 
$$N^* = \beta \frac{V_A}{V_F}$$
Note that this implies $\hat{h} = \beta$. 

#### Reasons for Hedging an Equity Portfolio

Why hedge using futures contracts at all when hedger can simply sell portfolio and invest proceeds in a risk-free instrument to earn the risk-free rate? 

- hedging can be justified if the hedger feels the stocks in the portfolio have been chosen well 
-- hedger might be uncertain about performance of market as a whole but confident in the stocks in the portfolio 
- hedger may be planning to hold a portfolio for a long period of time and requires short-term protection in an uncertain market situation 
-- alternative of selling the portfolio and buying it back could result in high transaction costs 

#### Changing the Beta of a Portfolio

To reduce the beta of the portfolio from $\beta$ to $\beta^*$, a short position in $$(\beta - \beta^*) \frac{V_A}{V_F}$$ contracts is required.

To increase the beta of the portfolio from $\beta$ to $\beta^*$, a long position in $$(\beta^* - \beta) \frac{V_A}{V_F}$$ contracts is required. 

## Stack and Roll

- expiration date of hedge may be later than the delivery dates of all futures contracts that can be used
-- hedger must roll the hedge forward by closing out one futures contract and taking the same position in a futures contract with a later delivery date 
-- hedges can be rolled forward many times (*stack and roll*) 
- can result in liquidity problems due to mismatch in cash inflow/outflow timings 


