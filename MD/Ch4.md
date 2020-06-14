# Ch 4 Interest Rates

## Types of Rates

- interest rate defines the amount of money a borrower promises to pay a lender

credit risk - risk there will be a default by the borrower

- higher credit risk means higher interest rate 

- interest rates often expressed in basis points 
-- 1 basis point = 0.01% per annum 

#### Treasury Rates

- rates an investor earns on Treasury bills and Treasury bonds
-- instruments used by a government to borrow in its own currency
-- assumed zero default risk so Treasury rates are risk-free rates 

#### LIBOR 

*London Interbank Offered Rate*

- unsecured short-term borrowing rate between banks 
- used as reference rates for transactions worldwide
- reasons to suggest manipulation of rates
-- make banks' borrowing costs seem lower than they actually are
-- to profit from transactions such as interest rate swaps whose cash flows depend on LIBOR fixings
- not enough interbank borrowing for banks to make accurate estimates of their borrowing rates
-- LIBOR quotes may be replaced by a smaller number of quotes based on actual transactions in a more liquid market 

#### Fed Funds Rate

- US financial institutions are required to maintain cash reservers with the Federal Reserve
-- reserve requirement depends on a bank's outstanding assets and liabilities
-- at end of day some banks have surplus and some need more funds 
-- leads to borrowing and lending overnight

federal funds rate - overnight rate 

#### Repo Rates

repo - repurchase agreement

- financial institution that owns securities agrees to sell the securities for a certain price and buy them back at a later time for a slightly higher price 
-- financial institution is obtaining a loan 
-- the interest rate it pays is the difference between the price at which the securities are sold and the price at which they are repurchased 
-- the interest rate is the *repo rate*
- repo rates are secured borrowing rates
-- generally slightly below the corresponding fed funds rate, which is an unsecured rate 
- a properly structured repo involves little credit risk 
-- if borrower does not honor the agreement, the lender simply keeps the securities 
-- if the lender does not honor the agreement, the original owner of the securities keeps the cash provided by the lender 
- most common type of repo is the *overnight repo* 
-- may be rolled over day to day 

#### The "Risk-Free" Rate

- derivates are valued using a risk-free interest rate as benchmark
- a number of different proxies for the risk-free rate are used 
-- LIBOR (though it is not actually risk-free) 

## Measuring Interest Rates

- meaning of an interest rate depends on the compounding frequency
- continuous compounding results in exponential growth 

## Zero Rates

- the *n*-year zero-coupon interest rate is the interest earned on an investment that starts today and lasts for *n* years
-- all interest and principal is realized at the end of *n* years 
-- no intermediate payments 

## Bond Pricing

- most bonds pay coupons to the holder periodically 
- the bond's principal (par value or face value) is paid at the end of its life 
- theoretical price of a bond can be calculated as the present value of all cash flows that will be received by the owner of the bond 

#### Bond Yield

- the single discount rate that, when applied to all cash flows, gives a bond price equal to its market price 

#### Par Yield

- the coupon rate that causes the bond price to equal its par value (principal)

## Determining Treasury Zero Rates

- observe the yield on "strips"
-- zero-coupon bonds synthetically created by traders when they sell coupons on a Treasury bond separately from the principal
- *bootstrap method*
-- determine Treasury zero rates from Treasury bills and coupon-bearing bonds 

zero curve - chart showing the zero rate as a function of maturity 

- calculated via linear interpolation 

## Forward Rates

- forward interest rates are the future rates of interest implied by current zero rates for periods of time in the future 

## Forward Rate Agreements

- an OTC transaction designed to fix the interest rate that will apply to either borrowing or lending a certain principal during a specified future period of time
-- usually assume borrowing or lending is done at LIBOR

- if agreed fixed rate is greater than the actual LIBOR rate for the period
-- borrower pays the lender the difference between the two applied to the principal
- if agreed fixed rate is less than the actual LIBOR rate for the period
-- lender pays the borrower the difference applied to the principal 

Consider an FRA where company X lends money to company Y for period of time $T_1$ to $T_2$

$R_K$ : fixed rate of interest agreed to in FRA
$R_F$ : forward LIBOR rate for period between $T_1$ and $T_2$ calculated today
$R_M$ : actual LIBOR rate observed in the market at $T_1$ for the period between $T_1$ and $T_2$
$L$ : principal underlying the contract 

Normally company X would earn $R_M$ from the loan. Due to the FRA it earns $R_K$. The extra interest (may be negative) as a result of the FRA is $R_K - R_M$. The interest rate is set at $T_1$ and paid at $T_2$. Thus the cash flow to company X at $T_2$ is $$L(R_K - R_M)(T_2 - T_1)$$
The cash flow to company Y at $T_2$ is $$L(R_M - R_K)(T_2 - T_1)$$

This gives rise to an alternative interpretation of an FRA. FRA is an agreement where:
- company X receives interest on the principal between $T_1$ and $T_2$ at fixed rate $R_K$ and pays interest at the realized LIBOR rate of $R_M$
- company Y pays interest on the principal between $T_1$ and $T_2$ at fixed rate $R_K$ and receives interest at the realized LIBOR rate of $R_M$ 

FRAs are usually settled at $T_1$ rather than at $T_2$, so payoff must be discounted from $T_2$ to $T_1$. 
Company X payoff at $T_1$ is $$\frac{L(R_K - R_M)(T_2 - T_1)}{1 + R_M(T_2 - T_1)}$$ Company Y payoff at $T_1$ is $$\frac{L(R_M - R_K)(T_2 - T_1)}{1 + R_M(T_2 - T_1)}$$

#### Valuation

- an FRA is worth zero when the fixed rate $R_K$ equals the forward rate $R_F$ 
-- at first, $R_K = R_F$ so value of contract to each side is zero
-- over time, interest rates change, so the value is nonzero

- market value of a derivative at a particular time is its *mark-to-market* (MTM) value

Value of FRA where $R_K$ is received $$V_{FRA} = L(R_K - R_F)(T_2 - T_1)e^{-R_2 T_2}$$
Value of FRA where $R_K$ is paid $$V_{FRA} = L(R_F - R_K)(T_2 - T_1)e^{-R_2 T_2}$$

## Duration

duration - measure of how long on average the holder of the bond has to wait before receiving cash payments 

- zero-coupon bond that lasts *n* years has a duration of *n* years 
- coupon-bearing bond lasting *n* years has a duration of less than *n* years 

A bond provides the holder with cash flows $c_i$ at time $t_i$. The bond price $B$ and bond yield $y$ are related by $$B = \sum_{i=1}^n c_i e^{-y t_i}$$ The duration of the bond is $$D = \frac{\sum_{i=1}^n t_i c_i e^{-y t_i}}{B} = \sum_{i=1}^n t_i \left[ \frac{c_i e^{-y t_i}}{B} \right]$$ The term is brackets is the ratio of the present value of the cash flow at time $t_i$ to the bond price. The bond price is the present value of all payments. 

Thus, the duration is a weighted average of the times when payments are made, where the weight at time $t_i$ is the proportion of the bond's total present value provided by the cash flow at time $t_i$.

With a small change $\Delta y$ in the yield, it is approximately true that $$\Delta B = \frac{dB}{dy} \Delta y$$ Plug this into the bond price equation to get $$\Delta B = - \Delta y \sum_{i=1}^n c_i t_i e^{-y t_i}$$ This results in the duration relationship $$\Delta B = -BD \Delta y$$ which can be written as $$\frac{\Delta B}{B} = -D \Delta y$$

---

DV01 is the price change from a 1-basis-point increase in all rates. 
Gamma is the change in DV01 from a 1-basis-point increase in all rates. 

---

#### Modified Duration

$$D^* = \frac{D}{1 + y/m}$$
The duration relationship can be simplified to $$\Delta B = -BD^* \Delta y$$ when $y$ is expressed with a compounding frequency of $m$ times per year 

*Dollar duration* is the product of modified duration and bond price $D_D = BD^*$ so that $$\Delta B = -D_D \Delta y$$

#### Bond Portfolios 

- the duration $D$ of a bond portfolio can be defined as a weighted average of the durations of individual bonds in the portfolio
-- weights proportional to bond prices 
- implicit assumption that the yields of all bonds will change by approximately the same amount
-- parallel shift in the zero-coupon yield curve 
- financial institutions can eliminate exposure to small parallel shifts in the yield curve
-- by choosing a portfolio where duration of assets equals duration of liabilities 
-- still exposed to shifts that are either large or nonparallel 

## Convexity

- the duration relationship applies only to small changes in yields 
- two bond portfolios with the same duration can behave differently for large yield changes
-- yield curves with different curvature

convexity - measure of curvature

$$C = \frac{1}{B}\frac{d^2 B}{dy^2} = \frac{\sum_{i=1}^n c_i t_i^2 e^{-yt_i}}{B}$$

Taylor series expansions give $$\Delta B = \frac{dB}{dy} \Delta y + \frac{1}{2} \frac{d^2 B}{dy^2} \Delta y^2$$ which leads to $$\frac{\Delta B}{B} = -D \Delta y + \frac{1}{2} C (\Delta y)^2$$

For a portfolio with a particular duration, the convexity tends to be greatest when the portfolio provides payments evenly over a long period of time. Convexity is least when payments are concentrated around one particular point in time. 

Financial institutions can become immune to large parallel shifts in the zero curve by choosing a portfolio of assets and liabilities with net duration of zero and net convexity of zero. However, it is still exposed to nonparallel shifts. 

## Theories of the Term Structure of Interest Rates

What determines the shape of the zero curve? 

- *expectations theory*
-- long-term interest rates should reflect expected future short-term interest rates 
-- a forward interest rate corresponding to a certain future period is equal to the expected future zero interest rate for that period 
- *market segmentation theory*
-- there need be no relationship between short, medium, and long-term interest rates 
-- investors invest in bonds of a certain maturity and do not readily switch from one maturity to another
- *liquidity preference theory*
-- investors prefer to preserve their liquidity and invest funds for short periods of time 
-- borrowers, though, prefer to borrow at fixed rates for long periods of time 
-- this causes forward rates to be greater than expected future zero rates 
-- consistent with empirical result that yield curves tend to be upward sloping more often than they are downward sloping 

#### The Management of Net Interest Income

net interest income - excess of the interest received over the interest paid 

Lenders prefer shorter-term investments for increased liquidity. 
Borrowers prefer longer-term investments to lock in a rate. 
This leads to mismatched maturities of assets and liabilities. 
Therefore long-term rates tend to be higher than those that would be predicted by expected future short-term rates. 
So the yield curve is upward sloping most of the time. 
It is downward sloping only when the market expects a steep decline in short-term rates. 

#### Liquidity

Portfolios where maturities are mismatched can lead to liquidity problems. 

