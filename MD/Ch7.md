# Ch 7 Swaps

swap - an OTC agreement between two companies to exchange cash flows in the future
- defines the dates when the cash flows are to be paid 
- defines the way in which the cash flows are to be calculated 

Forward contract can be viewed as a swap, with a cash flow exchange on just one future date. 

Swaps make up a majority of the OTC derivate market. 

- most popular (plan vanilla) interest rate swap is where LIBOR is exchanged for a fixed rate of interest 
- valuing swaps requires a "risk-free" discount rate for cash flows 
-- LIBOR is often used as proxy for the risk-free discount rate

## Mechanics of Interest Rate Swaps

interest rate swap - one company agrees to pay another company cash flows at a fixed rate and receives interest at a floating rate on some notional principal for a given time period 

#### LIBOR

- LIBOR is the floating rate in most interest rate swap agreements
- floating-rate payments on a payment date are calculated using the floating rate prevailing at the start of the payment period 
-- for example if the payment period is 6 months then use the rate 6 months prior to the payment date 
- the principal amount (*notional*) is used only for calculation of interest payments and is itself not exchanged 

This type of swap can be regarded as exchanging a fixed-rate bond for a floating-rate bond. 

#### Using the Swap to Transform a Liability

Swaps can be used to transform a floating-rate loan into a fixed-rate loan. 

Original: Pay LIBOR plus 0.1%. (floating-rate)
Swap: Receive LIBOR and pay fixed rate 5%. (transformation) 
Result: Pay fixed rate of 5.1%. (fixed-rate)

Swaps can be used to transform a fixed-rate loan into a floating-rate loan. 

Original: Pay fixed rate of 5.2%. (fixed-rate)
Swap: Pay LIBOR and receive fixed rate of 5%. (transformation)
Result: Pay LIBOR plus 0.2%. (floating-rate) 

#### Using the Swap to Transform an Asset

Swaps can be used to transform an asset earning fixed-rate into an asset earning floating-rate.

Original: Own $100m bonds providing interest at 4.7%. (fixed-rate)
Swap: Receive LIBOR and pay 5%. (transformation)
Result: Receive LIBOR - 0.3%. (floating-rate)

Swaps can be used to transform an asset earning floating-rate into an asset earning fixed-rate. 

Original: Invest $100m yielding LIBOR - 0.2%. (floating-rate)
Swap: Pay LIBOR and receive 5%. (transformation)
Result: Receive 4.8%. (fixed-rate) 

#### Role of Financial Intermediary

- financial institution enters into two offsetting swap transactions with the swap counterparties
- typically profit 3-4 basis points if neither party defaults 
-- compensation for risk that one of the two companies may default on the swap payments 

#### Market Makers

- unlikely that two companies contact a financial institution at the same time to take opposite position in exactly the same swap
- financial institutions act as market makers
-- enter into a swap without having an offsetting swap with another counterparty

## Day Count Issues

- day count conventions affect payments on a swap
- fixed payments may not be exactly equal on each payment date 

## Confirmations

confirmation - legal agreement underlying a swap, signed by representatives of the two parties

- defines terminology used in swap agreements
- specifies what happens if either side defaults
- specifies which days are business days and which days are holidays 
-- payment date on a weekend or holiday means payment is made on next business day 

## The Comparative-Advantage Argument

The popularity of swaps can be explained by comparative advantage. Some companies have a comparative advantage when borrowing in fixed-rate markets and other companies have a comparative advantage when borrowing in floating-rate markets. This can arise due to differences in credit ratings. 

#### Criticism of the Argument

Why have the differences not been arbitraged away?

- fixed-rate loans are given, for example, for 5 years 
- floating-rate loans are given, for example, for 6 months
-- lender can reassess creditworthiness of borrower every 6 months

## The Nature of Swap Rates

A financial institution can earn the 5-year swap rate by:
1. Lend principal for first 6 months to an AA borrower and then relend it for successive 6-month periods to other AA borrowers
2. Enter into a swap to exchange LIBOR for the 5-year swap rate 

Note that 5-year swap rates are less than 5-year AA borrowing rates. The difference is in lending money for successive 6-month periods to borrowers who are always AA at the beginning of the period rather than lending to one borrower for the whole 5 years. 

Swap rates are therefore sometimes called "continually refreshed" LIBOR rates. 

## Determining LIBOR/Swap Zero Rates

A problem with LIBOR rates is that direct observations are possible only for maturities out to 12 months. Eurodollar futures are used to extend the LIBOR zero curve beyond 12 months, usually out to 2 years. Swap rates can be used to further extend the LIBOR zero curve. The result is the *LIBOR/swap zero curve*. 

## Valuation of Interest Rate Swaps

An interest rate swap is worth close to zero at initiation. 
The value becomes positive or negative over time.

There are two valuation approaches: 
1. Regard the swap as the difference between two bonds
2. Regard the swap as a portfolio of FRAs 

#### Valuation in Terms of Bond Prices

Principal payments are not exchanged in an interest rate swap. 
However, assuming that principal payments are both received and paid at the end of the swap does not change the value of the swap. 

From the point-of-view of the floating-rate payer, a swap is a long position in a fixed-rate bond and a short position in a floating-rate bond $$V_{\text{swap}} = B_{\text{fix}} - B_{\text{fl}}$$

From the point-of-view of the fixed-rate payer, a swap is a long position in a floating-rate bond and a short position in a fixed-rate bond $$V_{\text{swap}} = B_{\text{fl}} - B_{\text{fix}}$$

Let the notional principal be $L$, the next exchange of payments be at time $t^*$, and the floating payment made at time $t^*$ be $k^*$. Immediately after the payment, $B_{\text{fl}} = L$. (Note that the bond is worth the notional principal immediately after a payment because at this time the bond is a "fair deal".) This means that immediately before the payment, $B_{\text{fl}} = L + k^*$. Regard the floating-rate bond as providing a single cash flow of $L + k^*$ at time $t^*$. Discount this to present value of $(L + k^*) e^{-r^* t^*}$ today, where $r^*$ is the LIBOR/swap zero rate for a maturity of $t^*$. 

#### Valuation in Terms of FRAs

A swap can be characterized as a portfolio of forward-rate agreements. 

The first exchange of payments is known at the time the swap is negotiated. 
The other exchanges can be regarded as FRAs. 

An FRA can be valued by assuming that forward interest rates are realized. 
A plain vanilla interest rate swap can be valued using the same assumption. 

1. Use the LIBOR/swap zero curve to calculate forward rates for each of the LIBOR rates that will determine swap cash flows.
2. Calculate swap cash flows on the assumption that the LIBOR rates will equal the forward rates. 
3. Discount these swap cash flows (using the LIBOR/swap zero curve) to obtain the swap value. 

## Term Structure Effects

A swap is worth close to zero at initiation. 

The sum of the values of the FRAs underlying the swap is close to zero. 
This does not mean the value of each individual FRA is close to zero. 

Suppose the term structure of interest rates is upward-sloping at the time of swap negotiation. 
This means forward interest rates increase as maturity of the FRA increases. 
The value of FRAs corresponding to early payment dates is negative.
The value of FRAs corresponding to later payment dates is positive. 

Suppose the term structure of interest rates is downward-sloping.
This means forward interest rates decrease as maturity of the FRA increases. 
The value of FRAs corresponding to early payment dates is positive.
The value of FRAs corresponding to later payments dates is negative.

## Fixed-for-Fixed Currency Swaps

- exchanging principal and interest payments at a fixed rate in one currency for principal and interest payments at a fixed rate in another currency
- requires principal to be specified in each of the two currencies
- principal amounts are usually exchanged at the beginning and at the end of the swap life 
-- usually chosen to be equivalent based on exchange rate at swap initiation 
-- values may be different when exchanged at end of life of the swap 

#### Use of a Currency Swap to Transform Liabilities and Assets

This type of swap can be used to transform borrowings in one currency to borrowings in another currency. 

#### Comparative Advantage

Currency swaps can be motivated by comparative advantage. 
A possible source of comparative advantage is tax. 

## Valuation of Fixed-for-Fixed Currency Swaps

Fixed-for-fixed currency swaps can be valued either by decomposing into the difference between two bonds or as a portfolio of forward contracts. 

#### Valuation in Terms of Bond Prices

The value of a swap where dollars are received and a foreign currency is paid is$$V_\text{swap} = B_D - S_0 B_F$$ 

$B_F$ is the value, measured in foreign currency, of the bond defined by foreign cash flows
$B_D$ is the value of the bond defined by domestic cash flows 
$S_0$ is the spot exchange rate (dollars per unit of foreign currency) 

The value of a swap where the foreign currency is received and dollars are paid is $$V_\text{swap} = S_0 B_F - B_D$$

#### Valuation as Portfolio of Forward Contracts

Each exchange of payments in a fixed-for-fixed currency swap is a forward foreign exchange contract. Assume that forward exchange rates are realized. 

Value of a currency swap is close to zero at initiation. 
If the two principals are worth the same at the start of the swap, the value of the swap is also close to zero immediately after the initial exchange of principal. 
This does not mean each of the individual forward contracts underlying the swap has a value close to zero. 

Suppose interest rates in two currencies are different. 

From point-of-view of payer of currency with high interest rate:
- forward contracts corresponding to early exchanges have negative value
- forward contracts corresponding to later exchanges have positive value 

From point-of-view of payer of currency with low interest rate:
- forward contracts corresponding to early exchanges have positive value
- forward contracts corresponding to later exchanges have negative value 

## Other Currency Swaps

Two other popular currency swaps:
1. Fixed-for-floating where a floating interest rate in one currency is exchanged for a fixed interest rate in another currency
2. Floating-for-floating where a floating interest rate in one currency is exchanged for a floating interest rate in another currency

## Credit Risk

Transactions such as swap that are private arrangements between companies entail credit risk.

Suppose value of swap to a financial institution is positive.
- the financial institution has credit-risk exposure because counterparty can default 

Suppose value of swap to a financial institution is negative.
- there is no effect on the financial institution, based on the assumption the defaulting counterparty will sell the transaction to a third party so its positive value is not lost 

Potential losses from defaults on a swap are less than potential losses from default on a loan. 
- swap value is a small fraction of value of the loan

Potential losses from defaults on a currency swap are greater than potential losses from default on an interest rate swap.
- principal amounts are exchanged in two different currencies at the end of life of a currency swap 
-- currency swap is liable to have a greater value at the time of default than an interest rate swap 

---
Credit risk vs Market risk

- credit risk arises from possibility of default by the counterparty when the value of the contract to the financial institution is positive 
- market risk arises from possibility that market variables (interest rates, exchange rates) will move in a way that causes the value of the contract to the financial institution to become negative 

Market risk can be hedged more easily than credit risk. 

- enter into offsetting contracts 

Banks trading swaps also bear legal risk. 

#### Central Clearing

Regulators may required standardized OTC derivatives to be cleared through central counterparties (CCPs).

- CCP acts as intermediary between the two sides in a transaction 
- requires initial margin and variation margin from both sides 
- purpose is to reduce credit risk in OTC markets 

#### Credit Default Swaps

- allows companies to hedge credit risks 
- insurance contract that pays off if a particular company or country defaults 

The buyer of credit protection pays an insurance premium (*CDS spread*) to the seller of protection for the life of the contract or until the *reference entity* defaults. 

The payoff in the event of default would be such that the buyer of protection is made whole. 

## Other Types of Swaps

#### Variations on the Standard Interest Rate Swap

- tenor (payment freq) on the floating side does not have to match tenor on the fixed side 
- commercial paper (CP) rate instead of LIBOR can be used as floating rate
- basis swap - a floating-floating interest rate swap where the floating rates have different bases (such as commercial paper for one and LIBOR for the other)
- amortizing swap - principal reduces in a predetermined way 
- step-up swap - principal increases in a predetermined way 
- forward swaps - parties do not begin to exchange payments until some future date 
- constant maturity swap - agreement to exchange a LIBOR rate for a swap rate 
- constant maturity Treasury swap - agreement to exchange a LIBOR rate for a Treasury rate 
- compounding swap - interest on one or both sides is compounded forward to end of life according to predetermined rules and there is only one payment date at the end of life
- LIBOR-in-arrears swap - LIBOR rate observed on a payment date is used to calculate the payment on that date (as opposed to using the LIBOR rate at start of payment period)
- accrual swap - interest on one side accrues only when the floating rate is in a certain range

#### Diff Swaps

Sometimes a rate observed in one currency is applied to a principal amount in another currency. 
Ex: 3-month LIBOR observed in the US is exchange for 3-month LIBOR in Britain, with both rates being applied to a principal of 10m British pounds. 

Also known as a **quanto**. 

#### Equity Swaps

Agreement to exchange the total return (dividends and capital gains) realized on an equity index for either a fixed or a floating rate of interest. Used to convert returns from a fixed or floating investment to the returns from investing in an equity index, and vice versa. 

#### Options

There can be options embedded in a swap agreement. 

- extendable swap - one party has the option to extend the life of the swap 
- puttable swap - one party has the option to terminate the swap early

swaptions - options on swaps
- provide one party with the right at a future time to enter into a swap where a predetermined fixed rate is exchanged for floating

#### Commodity Swaps, Volatility Swaps, and Other Exotic Instruments

commodity swaps - series of forward contracts on a commodity with different maturity dates and the same delivery prices 

volatility swap - series of time periods where at the end of each period, one side pays a predetermined volatility, while the other side pays the historical volatility realized during the period 

Swaps are limited only by the imaginations of financial engineers and the desire of treasurers and fund managers for exotic structures. 


