# Efficient Portfolio Construction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1SLOCZVNzx8zMBftkt5v8KA3CwtHMlguU?usp=sharing)

This is a Google Colaboratory (Jupyter notebook) implementation of [Robert C. Merton](https://en.wikipedia.org/wiki/Robert_C._Merton)'s efficient portfolio algorithm from the paper *An Analytic Derivation of the Efficient Portfolio Frontier* (1972).

In the paper, Merton identifies an algorithm that, given historical returns data from several identified securities, constructs a portfolio with the <ins>lowest variance in returns for a given level of expected returns</ins> (this is the "efficiency").

The algorithm outputs the fraction of the portfolio to be allocated to each security. Each may be positive or negative corresponding to long and short positions, or zero when no position should be taken. They are guaranteed to sum to 100%.

The linked notebook as written returns such a portfolio using some or all constituents of the S&P 100 index with available returns data from 2010-2019. You must specify the level of expected returns at which to perform the allocation.

**Keep in mind the portfolio is only efficient for time periods with available returns data. The results are not forward-looking, nor are they advice to buy or sell any security.**

```
Assumed total annual return: 25.0%.

Minimium-variance portfolio is:
X(AAPL) = 12.0% (LONG)
X(ABT) = 4.0% (LONG)
X(ACN) = -9.0% (SHORT)
X(ADBE) = 1.0% (LONG)
X(AIG) = -1.0% (SHORT)
X(ALL) = 13.0% (LONG)
X(AMGN) = 2.0% (LONG)
X(AMT) = 38.0% (LONG)
X(AMZN) = -3.0% (SHORT)
X(AXP) = -20.0% (SHORT)
X(BA) = 11.0% (LONG)
X(BAC) = 5.0% (LONG)
X(BIIB) = -5.0% (SHORT)
X(BK) = -1.0% (SHORT)
X(BKNG) = 1.0% (LONG)
X(BLK) = 6.0% (LONG)
X(BMY) = 14.0% (LONG)
X(BRK-B) = 17.0% (LONG)
X(C) = 7.0% (LONG)
X(CAT) = -14.0% (SHORT)
X(CHTR) = -4.0% (SHORT)
X(CL) = -11.0% (SHORT)
X(CMCSA) = -1.0% (SHORT)
X(COF) = 4.0% (LONG)
X(COP) = -13.0% (SHORT)
X(COST) = -35.0% (SHORT)
X(CRM) = 2.0% (LONG)
X(CSCO) = -11.0% (SHORT)
X(CVS) = -2.0% (SHORT)
X(CVX) = 2.0% (LONG)
X(DD) = 3.0% (LONG)
X(DHR) = 17.0% (LONG)
X(DIS) = -17.0% (SHORT)
X(DUK) = 4.0% (LONG)
X(EMR) = 6.0% (LONG)
X(EXC) = 4.0% (LONG)
X(F) = -2.0% (SHORT)
X(FDX) = 3.0% (LONG)
X(GD) = -7.0% (SHORT)
X(GE) = -1.0% (SHORT)
X(GILD) = -2.0% (SHORT)
X(GM) = -4.0% (SHORT)
X(GOOG) = 2.0% (LONG)
X(GOOGL) = 0.0% (LONG)
X(GS) = -3.0% (SHORT)
X(HD) = 9.0% (LONG)
X(HON) = -2.0% (SHORT)
X(IBM) = -12.0% (SHORT)
X(INTC) = -1.0% (SHORT)
X(JNJ) = 5.0% (LONG)
X(JPM) = -6.0% (SHORT)
X(KO) = 5.0% (LONG)
X(LLY) = -6.0% (SHORT)
X(LMT) = -1.0% (SHORT)
X(LOW) = 3.0% (LONG)
X(MA) = 6.0% (LONG)
X(MCD) = 17.0% (LONG)
X(MDLZ) = -7.0% (SHORT)
X(MDT) = -7.0% (SHORT)
X(MET) = -8.0% (SHORT)
X(MMM) = -3.0% (SHORT)
X(MO) = 18.0% (LONG)
X(MRK) = 40.0% (LONG)
X(MS) = 2.0% (LONG)
X(MSFT) = -3.0% (SHORT)
X(NEE) = -2.0% (SHORT)
X(NFLX) = 2.0% (LONG)
X(NKE) = -2.0% (SHORT)
X(NVDA) = -4.0% (SHORT)
X(ORCL) = 8.0% (LONG)
X(OXY) = 1.0% (LONG)
X(PEP) = -11.0% (SHORT)
X(PFE) = -1.0% (SHORT)
X(PG) = -11.0% (SHORT)
X(PM) = 1.0% (LONG)
X(QCOM) = 0.0% (LONG)
X(RTX) = 2.0% (LONG)
X(SBUX) = 14.0% (LONG)
X(SLB) = 0.0% (LONG)
X(SO) = 5.0% (LONG)
X(SPG) = -2.0% (SHORT)
X(T) = 12.0% (LONG)
X(TGT) = -3.0% (SHORT)
X(TMO) = -3.0% (SHORT)
X(TXN) = 1.0% (LONG)
X(UNH) = 12.0% (LONG)
X(UNP) = -4.0% (SHORT)
X(UPS) = 4.0% (LONG)
X(USB) = -3.0% (SHORT)
X(V) = 4.0% (LONG)
X(VZ) = 32.0% (LONG)
X(WBA) = 8.0% (LONG)
X(WFC) = 1.0% (LONG)
X(WMT) = -7.0% (SHORT)
X(XOM) = -13.0% (SHORT)

Sum of X = 100.0%
```
If $10,000 was invested with that allocation (and rebalanced monthly) between January 2011 and December 2019 the portfolio would have had the following returns:
<img src="example_analysis/portfolio_growth.png" alt="growth" width="100%"/>
<img src="example_analysis/annual_returns.png" alt="returns" width="100%"/>
<img src="example_analysis/drawdowns.png" alt="drawdowns" width="100%"/>
