# Ch 9 OIS Discounting, Credit Issues, and Funding Costs

## The Risk-Free Rate

The choice of risk-free rate is important for valuing derivatives.

Rates on Treasury bills, Treasury notes, and Treasury bonds are not used because they are artificially low for the following reasons:
1. Treasury bills and bonds must be purchased by financial institutions to fulfill regulatory requirements, which increases demand for these and drives the price up and the yield down.
2. The amount of capital a bank is required to hold to support an investment in these is smaller than the requirement to support investments in other instruments with low risk.
3. Treasury instruments are given a favorable tax treatment compared with other fixed-income investments because they are not taxed at the state level. 

LIBOR was typically used as the risk-free rate. LIBOR rates soared during the credit crisis because banks were reluctant to lend to each other. Banks began using overnight indexed swap (OIS) rates for collateralized transactions and continued to use LIBOR for non-collateralized transactions. This reflects a belief that the discount rate should represent a derivative's average funding costs rather than using a true risk-free rate. 

## The OIS Rate

fed funds rate - overnight unsecured borrowing interest rate between US financial institutions
effective fed funds rate - weighted average of rates in brokered transactions 

overnight indexed swap (OIS) - swap where a fixed rate for a period is exchanged for the geometric average of the overnight rates during the period 

OIS rate - fixed rate in an OIS 

---

OIS rate is generally lower than LIBOR because the risk of default on a 3-month LIBOR loan is greater than the risk of default on a 3-month OIS. This is because overnight lenders have the option of ceasing to lend if the borrower's credit quality declines. 

The excess of the LIBOR rate over the OIS rate is the *LIBOR-OIS spread*. 

The OIS rate is a good proxy for the risk-free rate. 

It has two small sources of risk:
1. Default on an overnight loan between two financial institutions. 
2. Default on the OIS swap itself. 

## Valuing Swaps and FRAs with OIS Discounting

#### Determining Forward LIBOR Rates with OIS Discounting

LIBOR-for-fixed swaps can be valued assuming that forward LIBOR rates are realized. 
LIBOR forward rates given by OIS discounting are different from those given by LIBOR discounting. 

## OIS vs LIBOR: Which is Correct?

Most derivatives dealers use discount rates based on OIS rates when valuing collateralized derivatives and discount rates based on LIBOR when valuing non-collateralized derivatives. 

This is due to funding costs. 

Collateralized derivatives are funded by collateral and the federal funds rate is the overnight interest rate most commonly paid on collateral. For non-collateralized derivatives, funding costs are higher so the discount rate should reflect this. 

Arguments based on funding costs are questionable. It is long-established that evaluation of an investment should not depend on the way it is funded. Only the risk and expected cash flows are important. Since OIS rate is as close to risk-free as possible, it should be used for both collateralized and non-collateralized transactions. 

## Credit Risk: CVA and DVA

credit value adjustment (CVA) - present value of the expected cost to the bank of a counterparty default 

Suppose the life of the longest outstanding derivatives transaction between the bank and the counterparty is $T$ years. To calculate CVA, the bank divides the $T$ years into intervals. 
For each interval, calculate:
1. Probability of early termination during the interval arising from counterparty default, $q_i$
2. Present value of expected loss of the derivatives portfolio if there is early termination, $v_i$

$$\text{CVA} = \sum_{i=1}^N q_i v_i$$

Let $f_\text{nd}$ be the no-default value of the derivatives portfolio to the bank. 
When possibility of default is taken into account, the portfolio value becomes $$f_\text{nd} - \text{CVA}$$

The bank itself may default, which can lead to a loss to the counterparty with an equal and opposite gain to the bank. 

debt value adjustment (DVA) - present value of the expected gain to the bank from its own default 

$$\text{DVA} = \sum_{i=1}^N q_i^* v_i^*$$

where $q_i^*$ is the probability of default by the bank during the $i$th interval 
and $v_i^*$ is the present value of the bank's gain (and counterparty's loss) if the bank defaults at the midpoint of the interval. 

Thus the value of the portfolio to the bank is $$f_\text{nd} - \text{CVA} + \text{DVA}$$

#### Collateral

When the agreement between two parties requires collateral, calculations are more complicated for two reasons:
1. Collateral affects calculation of CVA and DVA
2. Interest rate paid on cash collateral may influence valuations

Collateral can usually consist of cash or marketable securities. 

Interest is normally paid on cash collateral. 
If the interest is the risk-free rate, no adjustment to valuation is needed. 
If the interest is not the risk-free rate, must estimate the excess of the present value of actual net interest over net interest paid at risk-free rate. This is the collateral rate adjustment (CRA). 

The value of the portfolio is $$f_\text{nd} - \text{CVA} + \text{DVA} - \text{CRA}$$

Banks assume OIS rate is the risk-free rate. If the effective federal funds rate is paid on overnight cash collateral balances, no CRA adjustment is needed. 

## Funding Costs

When banks assess whether to undertake a project, they should use the risk-free rate rather than the average funding cost. If the average funding cost is used as a hurdle rate for all projects, then low-risk projects will seem unattractive and high-risk projects will seem attractive, so banks will gravitate to higher-risk projects. 

Some consider funding costs to be relevant in derivatives valuation. They make a funding value adjustment (FVA) for non-collateralized derivatives. The purpose of FVA is to change the value of a derivative to what it would be if the bank's average funding cost were used the risk-free discount rate. 

FVA adjustments are controversial. 


