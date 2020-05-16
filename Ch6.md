# Ch 6 Interest Rate Futures

## Day Count and Quotation Conventions

#### Day Counts

- day count defines the way in which interest accrues over time 
- express as $X/Y$ 
-- $X$ defines the way in which the number of days between two dates is calculated
-- $Y$ defines the way in which the total number of days in the reference period is measured 

The interest earned between the two dates is $$\frac{\text{Number of days between dates}}{\text{Number of days in reference period}} \times \text{Interest earned in reference period }$$

Three days count conventions are commonly used in the US:
1. Actual/actual 
2. 30/360
3. Actual/360

- The actual/actual day count is used for Treasury bonds in the US 
- The 30/360 day count is used for corporate and municipal bonds in the US
- The actual/360 day count is used for money market instruments in the US 

#### Price Quotations of US Treasury Bills

- prices of money market instruments are sometimes quoted using a *discount rate*

discount rate - interest earned as a percentage of the final face value 
(rather than as a percentage of the initial price paid for the instrument) 

- Treasury bills in the US 

#### Price Quotations of US Treasury Bonds

- quoted in dollars and thirty-seconds of a dollar
- quoted price is for a bond with a face value of $100 

The quoted price is the *clean price* and the cash price paid by the purchaser is the *dirty price*. 
$$\text{Cash price} = \text{Quoted price} + \text{Accrued interest since last coupon date}$$

## Treasury Bond Futures

#### Quotes

Treasury bond futures are quoted in dollars and thirty-seconds of a dollar per $100 face value. 
Contracts specified as 144-20 means 144 $\frac{20}{32}$ or 144.625. 

The settlement price of 10-year Treasury note futures contract is quoted to the nearest half of a thirty-second. 
Settlement price of 131-025 means 131 $\frac{2.5}{32}$ or 131.078125. 

The 5-year and 2-year Treasury note contracts are quoted even more precisely, to the nearest quarter of a thirty-second. 

#### Conversion Factors

When a bond is delivered, the *conversion factor* defines the price received for the bond by the party with the short position. Cash received for each $100 face value of the bond delivered is $$(\text{Most recent settlement price} \times \text{Conversion factor}) + \text{Accrued interest}$$

#### Cheapest-to-Deliver Bonds

At any time during delivery month, there are many bonds that can be delivered in the Treasury bond futures contract. These vary widely in terms of coupon and maturity. 

The party with short position can choose which bond is cheapest to deliver. 

---
The cash received is $$(\text{Most recent settlement price} \times \text{Conversion factor}) + \text{Accrued interest}$$ and the cost of purchasing a bond is $$\text{Quoted bond price} + \text{Accrued interest}$$ so the cheapest-to-deliver bond is the one for which $$\text{Quoted bond price} - (\text{Most recent settlement price} \times \text{Conversion factor})$$ is the least. 

---

One the party with short position has decided to deliver, it can determine which is cheapest-to-deliver by examining each of the deliverable bonds. 

#### Determining the Futures Price

Assume the cheapest-to-deliver bond and delivery date are known. 
The Treasury bond futures contract is a futures contract on a traded security that provides known income. $$F_0 = (S_0 - I) e^{rT}$$ where $I$ is the present value of the coupons during the life of the futures contract, $T$ is the time until the futures contract matures, and $r$ is the risk-free interest rate applicable to a time period of length $T$. 

## Eurodollar Futures

Eurodollar - dollar deposited in a US or foreign bank outside the US 
Eurodollar interest rate - rate of interest earned on Eurodollars deposited by one bank with another bank 

#### Forward vs Futures Interest Rates

Eurodollar futures contract is similar to a forward rate agreement (FRA). 
- locks in an interest rate for a future period

For short maturities, Eurodollar futures interest rate can be assumed to be the same as the corresponding forward interest rate.

For longer contracts, there are important differences between the contracts.

---
Eurodollar futures contract on an interest rate for period between times $T_1$ and $T_2$ 
- settled daily
- final settlement at time $T_1$

FRA on an interest rate for period between times $T_1$ and $T_2$ 
- not settled daily
- final settlement at time $T_2$ 

Both reason decrease the forward rate relative to the futures rate. 

#### Convexity Adjustment 

A *convexity adjustment* accounts for the total difference between the two rates.
$$\text{Forward rate} = \text{Futures rate} - \frac{1}{2} \sigma^2 T_1 T_2$$ where $T_1$ is time to maturity of the futures contract, $T_2$ is time to maturity of the rate underlying the futures contract, and $\sigma$ is the standard deviation of the change in the short-term interest rate in 1 year. 

## Duration-Based Hedging Strategies Using Futures

Consider situation where a position in an asset that is interest-rate dependent (such as bond portfolio or money market security) is being hedged using an interest rate futures contract.

$V_F$ : Contract price for one interest rate futures contract
$D_F$ : Duration of asset underlying futures contract at maturity of contract
$P$ : Forward value of the portfolio being hedged at the maturity of the hedge 
$D_P$ : Duration of the portfolio at the maturity of the hedge

Assume change in yield $\Delta y$ is the same for all maturities (only parallel shifts of the yield curve). 

It is approximately true that $$\Delta P = -PD_P \Delta y$$ and that $$\Delta V_F = -V_F D_F \Delta y$$

The number of contracts required to hedge against an uncertain $\Delta y$ is $$N^* = \frac{PD_P}{V_F D_F}$$

This is the **duration-based hedge ratio** or the **price sensitivity hedge ratio**. 
It has the effect of making the duration of the entire position zero. 

---
- hedger must base $D_F$ on assumption that one particular bond will be delivered
- estimate which of the available bonds is likely to be cheapest to deliver 
- hedge must be adjusted if environment changes and another bond becomes cheapest
-- performance of hedge may be worse than anticipated 

---

Interest rates and futures prices move in opposite directions. 

- when interest rates go up, interest rate futures price goes down 
- when interest rates go down, interest rate futures price goes up 

A company that would lose money if interest rates drop should hedge by taking a long futures position. 
A company that would lose money if interest rates rise should hedge by taking a short futures position. 

## Hedging Portfolios of Assets and Liabilities 

Financial institutions hedge against interest rate risk by ensuring average duration of assets equals average duration of liabilities. This is called *duration matching* or *portfolio immunization*. 
It ensures that small parallel shifts in interest rates have little effect on the value of the portfolio. 

This does not protect against nonparallel shifts in the zero curve. 
Short-term rates are usually more volatile than long-term rates. 
Short-term and long-term rates are not correlated and may move in opposite directions.

Financial institutions have developed other tools to manage interest rate exposure. 
