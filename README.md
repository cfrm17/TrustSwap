# Trust Swap

The Canada Housing Trust Swap includes variable rate mortgages and involves reinvestments made by the principal payments. The variable rate mortgages that appear in 
the deal are a result of these reinvestment. The model was in the context of the much more complicated problem where the notional on the mortgages was not fixed, 
and reinvestments were made at prevailing market prices.

The issue of valuation is very much simplified by the fact that these variable rate mortgage principals pay interest based on one month BA, and this rate resets 
monthly.The prepayment is not an issue with these mortgages, since the principal is replaced (at par) in the event of prepayment and the floating rate payments 
remain one month BA. Therefore, valuing these assets is a simple exercise of valuing them equivalent to a floating rate bond.

These amount to floating rate payments based on one month BA. The principal on which the interest payments are made will remain constant in the event of principal 
payments (both scheduled and unscheduled prepayments). Therefore, valuing this asset is a very simple calculation, with the results being very close to par and equal 
to par if the valuation date is right after the payment date. In fact, it is equivalent to valuing a floating rate bond with fixed notional.

The discount curve used for valuation is based on risk free rates. The interest accrued is also based on these rates, and the day count convention for the interest 
payment is also ACT / 365. Immediately after payment date, the value of the mortgage is par, equal to a floating rate bond.

In the event that the valuation date is in between payment dates, the value of the “mortgage” is not equal to par. Let t0 is the last reset date, tv is the valuation 
date and t1 is the next interest payment. Also, let r0 correspond to the last reset rate. On the valuation date, we let ro correspond to the overnight BA rate and 
r1m correspond to the 30 day BA rate. Since the valuation date is between monthly swap payment dates, it is necessary to interpolate the effective BA rate.

The valuation of the variable rate mortgage, as it contributes to the CHT swap is very simple. It is simplified by the fact that the interest rate payable is fixed 
at 30 day BA, and that we are discounting using the same curve that is used to evaluate the interest received. Furthermore, the principal payments on the variable 
rate mortgages, including prepayments, are reinvested at par so that the principal remains constant.

If this were not the case, it would be very difficult to properly value the cashflows form the mortgage. One would have to specify how the mortgage prepayed, and 
of course this would very dependent on relevant interest rates. Because of the interest rate dependence on the cashflows, this quickly becomes a path dependent 
problem with Monte Carlo required for valuation. It would be even more complicated if the cashflows were for example based on prime, since one would then need to 
have a model for how the prime rate and the interest rates are correlated.

Reference:

https://finpricing.com/FinPricing-ProductBrochure.pdf
