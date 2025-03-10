# Factsheet: PEF_3-5 Corporate Bond Financing

- [Factsheet: PEF\_3-5 Corporate Bond Financing](#factsheet-pef_3-5-corporate-bond-financing)
  - [Core Concepts](#core-concepts)
    - [Types of Bonds](#types-of-bonds)
  - [Valuation Rules \& Equivalent Portfolios](#valuation-rules--equivalent-portfolios)
    - [Zero Bond Valuation](#zero-bond-valuation)
      - [Present Value (PV):](#present-value-pv)
      - [**Equivalent Portfolio**:](#equivalent-portfolio)
    - [Coupon Bond Valuation](#coupon-bond-valuation)
      - [PV (Dirty Price):](#pv-dirty-price)
      - [Clean price (market price):](#clean-price-market-price)
      - [Yield to Maturity (YTM):](#yield-to-maturity-ytm)
      - [Discount Factor:](#discount-factor)
      - [**Equivalent Portfolio**:](#equivalent-portfolio-1)
    - [Floater (Floating-Rate Bond) Valuation](#floater-floating-rate-bond-valuation)
      - [At coupon adjustment dates, PV equals face value.](#at-coupon-adjustment-dates-pv-equals-face-value)
      - [Between coupon dates:](#between-coupon-dates)
      - [**Equivalent Portfolio**:](#equivalent-portfolio-2)
    - [Convertible Bond](#convertible-bond)
      - [**Equivalent Portfolio**:](#equivalent-portfolio-3)
    - [Warrant Bond](#warrant-bond)
      - [**Equivalent Portfolio**:](#equivalent-portfolio-4)
  - [Bonds with Credit Risk](#bonds-with-credit-risk)
      - [Present Value:](#present-value)
      - [Expected Cash Flow:](#expected-cash-flow)
  - [Interest Rate Term Structures](#interest-rate-term-structures)
  - [Forward Rate and Forward Rate Agreement (FRA)](#forward-rate-and-forward-rate-agreement-fra)
      - [Forward rate ($f$) from $T\_1$ to $T\_2$:](#forward-rate-f-from-t_1-to-t_2)
      - [**Equivalent Portfolio**:](#equivalent-portfolio-5)
  - [Interest Rate Swap (IRS)](#interest-rate-swap-irs)
      - [Market Value (MV):](#market-value-mv)
      - [**Equivalent Portfolio**:](#equivalent-portfolio-6)
  - [Duration](#duration)
    - [Modified Duration (MD)](#modified-duration-md)
    - [Special Durations](#special-durations)
      - [**Zero Bond**:](#zero-bond)
      - [**Annuity Bond**:](#annuity-bond)
      - [**Perpetual Bond**:](#perpetual-bond)
  - [Key Definitions](#key-definitions)


## Core Concepts

### Types of Bonds

- **Zero Bond**: Pays no interim interest; full repayment at maturity.
- **Coupon Bond**: Pays regular coupons; principal repaid at maturity.
- **Floater (Floating-Rate Bond)**: Coupon adjusted periodically based on a benchmark rate (e.g., EURIBOR).
- **Convertible Bond**: Convertible into a fixed number of shares.
- **Warrant Bond**: Bond combined with call options (warrants) on shares.
- **Bonds with Credit Risk**: Bonds with default risk; repayment uncertain.

## Valuation Rules & Equivalent Portfolios

### Zero Bond Valuation
#### Present Value (PV):
  $$\text{PV}(Z) = Z \times P(T)$$
#### **Equivalent Portfolio**: 
Single zero bond replicating the bond’s payoff.

### Coupon Bond Valuation
#### PV (Dirty Price):
  $$\text{PV}(\text{Bond}) = \sum_{j=1}^{J} Z_j \times P(T_j)$$
#### Clean price (market price):
  $$\text{Clean Price} = \text{PV (Dirty price)} - \text{Accrued Interest}$$
  $$\text{Accrued Interest} = \text{Coupon} \times \frac{\text{days since last coupon}}{\text{days in coupon period}}$$
#### Yield to Maturity (YTM):
  $$\text{PV} = \sum_{j=1}^{J}\frac{Z_j}{(1+YTM)^{T_j}}$$
#### Discount Factor:
  $P(T_j) = \frac{1}{(1+R_j)^{T_j}}$ where $R_j$ is the spot rate at maturity $T_j$.
#### **Equivalent Portfolio**: 
Portfolio of zero bonds matching each coupon and principal payment.

### Floater (Floating-Rate Bond) Valuation
#### At coupon adjustment dates, PV equals face value.
#### Between coupon dates:
$$
\text{PV}_{t1} = (100 \times C_{t1}) \times P_{t1,t2}
$$
Here, "100" is the face value, and $C_{t1}$ is the coupon rate at date $t1$.
$P_{t1,t2}$ is the discount factor between $t1$ and next coupon date $t2$.
#### **Equivalent Portfolio**: 
Short-term zero bond reinvested at each coupon adjustment date.

### Convertible Bond
Convertible into shares at holder’s option, allowing participation in share price appreciation while still providing regular bond interest if conversion is unfavorable.
#### **Equivalent Portfolio**: 
Standard bond plus call option on shares.

### Warrant Bond
Bond with attached warrants (call options on shares).
#### **Equivalent Portfolio**: 
Standard bond plus separate warrants.

## Bonds with Credit Risk
Valuation considers Probability of Default (PD) and Recovery Rate.
#### Present Value:
  $$\text{PV} = \frac{\text{Expected Cash Flow}}{(1+YTM)}$$
#### Expected Cash Flow:
  $$\text{Expected CF} = (1-\text{PD}) \times \text{Face Value} + \text{PD} \times \text{Recovery Rate} \times \text{Face Value}$$
Yield spreads increase with higher credit risk (lower rating).

## Interest Rate Term Structures
- **Normal**: Upward-sloping; longer maturities yield higher rates.
- **Flat**: Similar yields across maturities.
- **Inverted**: Downward-sloping; short-term yields exceed long-term yields (often precedes recessions).

## Forward Rate and Forward Rate Agreement (FRA)
FRA locks future borrowing/investing rates; compensatory payments adjust for differences between agreed forward rate ($f$) and realized spot rate ($r$):
  $$\text{CP} = \frac{F \times (f - r)}{1 + r}$$
#### Forward rate ($f$) from $T_1$ to $T_2$:
  $$f_{T1,T2} = \frac{(1+R_{T2})^{T2}}{(1+R_{T1})^{T1}} - 1$$
#### **Equivalent Portfolio**:
  - FRA Short (lending): Long zero bond (longer maturity), short zero bond (shorter maturity).
  - FRA Long (borrowing): Short zero bond (longer maturity), long zero bond (shorter maturity).

## Interest Rate Swap (IRS)
Exchange fixed and floating interest payments.
#### Market Value (MV):
  $$\text{MV}(\text{IRS}) = \text{MV}(\text{Receiver leg}) - \text{MV}(\text{Payer leg})$$
#### **Equivalent Portfolio**:
  - IRS Receiver: Long coupon bond, short floater.
  - IRS Payer: Short coupon bond, long floater.

## Duration
Used in sensitivity of bond price to interest rate changes measurement:
  $$D = \frac{\sum_{j=1}^{J}PV(Z_j) \times T_j}{PV}$$

### Modified Duration (MD)
- Approximate % PV change for a 1% rate change:
  $$MD = \frac{D}{1+r}, \quad \Delta PV \approx -MD \times PV \times \Delta r$$

### Special Durations
#### **Zero Bond**:
  $$D = n$$
#### **Annuity Bond**:
  $$D = \frac{1+r}{r} - \frac{n}{(1+r)^n - 1}$$
#### **Perpetual Bond**:
  $$D = \frac{1+r}{r}$$

## Key Definitions
- **Discount Factor ($P(T)$)**: Present value of 1 currency unit at time T.
- **Spot Rate ($R$)**: Yield of a zero-coupon bond.
- **Yield to Maturity (YTM)**: Annualized return if bond held to maturity.