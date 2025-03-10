# Factsheet: PEF_2 Credit Financing
- [Factsheet: PEF\_2 Credit Financing](#factsheet-pef_2-credit-financing)
  - [Core Concepts](#core-concepts)
    - [Features and Roles of Debt](#features-and-roles-of-debt)
    - [Rating (Credit Scoring)](#rating-credit-scoring)
  - [Short-Term Credit Financing](#short-term-credit-financing)
    - [Implied Interest Cost Formula (Supplier Credit)](#implied-interest-cost-formula-supplier-credit)
    - [Overdraft Facility (Kontokorrentkredit)](#overdraft-facility-kontokorrentkredit)
      - [Cost Factors of Overdraft Facilities](#cost-factors-of-overdraft-facilities)
    - [Interest Calculation (Overdraft Facility)](#interest-calculation-overdraft-facility)
      - [**Interest cost per sub-period ($Z\_t$)**:](#interest-cost-per-sub-period-z_t)
      - [**Zinszahl (ZZ)**: changes over time](#zinszahl-zz-changes-over-time)
      - [**Zinsteiler (ZT)**: is constant. Different Banks may offer different rates, which can be compared.](#zinsteiler-zt-is-constant-different-banks-may-offer-different-rates-which-can-be-compared)
      - [**Total interest costs**:](#total-interest-costs)
  - [Long-Term Credit Financing](#long-term-credit-financing)
    - [Debt Service Payment](#debt-service-payment)
    - [Repayment Structures](#repayment-structures)
      - [**Repayment at maturity**: Full repayment at the end.](#repayment-at-maturity-full-repayment-at-the-end)
      - [**Installment Repayment**: Constant annual repayment amount:](#installment-repayment-constant-annual-repayment-amount)
      - [**Annuity Payments**: Constant debt-service amount:](#annuity-payments-constant-debt-service-amount)
  - [Market Value Calculation](#market-value-calculation)
      - [**If a market value is available (e.g., for an issued bond):**](#if-a-market-value-is-available-eg-for-an-issued-bond)
      - [**If a market value is not available (e.g., a bank loan):**](#if-a-market-value-is-not-available-eg-a-bank-loan)
  - [Loan Formula](#loan-formula)
      - [**Available funds at $t=0$:**](#available-funds-at-t0)
      - [**Cost of Capital (Approximative Yield to Maturity):**](#cost-of-capital-approximative-yield-to-maturity)
      - [**Mean Time to Maturity**:](#mean-time-to-maturity)
      - [**Exact Yield (Internal Rate of Return - IRR)**:](#exact-yield-internal-rate-of-return---irr)


## Core Concepts

### Features and Roles of Debt
- Debt: Pure financing function
- Equity functions: Establishment, Liability, Profit distribution, Solvency, Leadership

### Rating (Credit Scoring)
- **Probability of Default (PD)**: Estimated risk of borrower not repaying.
- Higher PD → Higher interest costs
- Rating sources:
  - Hard facts (financial statements, payment history)
  - Soft facts (management quality, industry position)

## Short-Term Credit Financing
- **Customer Prepayments**: Interest-free advance from customers.
- **Supplier Credit**: Extended payment terms from suppliers; implicit high interest via discounts.

### Implied Interest Cost Formula (Supplier Credit)
$$
\text{Implied Interest Cost} = \frac{\text{Discount}}{\text{Period Allowed} - \text{Discount Period}} \times 365
$$

### Overdraft Facility (Kontokorrentkredit)
- Short-term, revolving credit line.
- Costs: Debit interest, credit commission, overdraft commission

#### Cost Factors of Overdraft Facilities
- **Debit Interest**: Cost incurred for using credit funds.
- **Credit Interest**: Interest gained for positive balance.
- **Credit Commission Calculation Methods:**
  - Based on the total credit line (idle costs)
  - Based on monthly or quarterly peak usage (peak demand)
  - Based on unused portion of the credit line
- **Overdraft Commission**: Additional costs if the credit line is exceeded.

### Interest Calculation (Overdraft Facility)
#### **Interest cost per sub-period ($Z_t$)**:
$$
Z_t = \frac{\text{Balance}_t \times r \times \text{(\# of days)}_t}{100 \times (360 \text{ or } 365)}
$$

#### **Zinszahl (ZZ)**: changes over time

$$
\text{ZZ}_t = \frac{\text{Balance}_t \times \text{\#days}_t}{100}
$$

#### **Zinsteiler (ZT)**: is constant. Different Banks may offer different rates, which can be compared.

$$
ZT = \frac{360 \text{ or } 365}{r}
$$

#### **Total interest costs**:

$$
\text{Interest costs} = \frac{\sum ZZ_t}{ZT}
$$

## Long-Term Credit Financing
- Components: Amount paid out, repayment structure, interest rate, duration, collateral

### Debt Service Payment
$$
\text{Debt Service}_t = \text{Repayment}_t + \text{Interest}_t + \text{Fees}_t
$$

### Repayment Structures
#### **Repayment at maturity**: Full repayment at the end.
#### **Installment Repayment**: Constant annual repayment amount:
$$
T = \frac{K_0}{n}, \quad Z_t = i \times K_0 \times \left(1 - \frac{t - 1}{n}\right)
$$

#### **Annuity Payments**: Constant debt-service amount:
$$
A = K_0 \times \frac{i \times q^n}{q^n - 1}, \quad q = 1+i
$$

## Market Value Calculation
#### **If a market value is available (e.g., for an issued bond):**
$$
MV_j = \sum_{t=1}^{T} \frac{CF(t)_j}{(1+y_j)^t}
$$
  - $MV_j$: Market value of debt position $j$
  - $CF(t)_j$: Cash flow (debt service payment) at time $t$ for debt position $j$
  - $y_j$: Yield to maturity of debt position $j$

#### **If a market value is not available (e.g., a bank loan):**
$$
100 = \sum_{t=1}^{T} \frac{CF(t)_j}{(1+y_j)^t}
$$

## Loan Formula
#### **Available funds at $t=0$:**
$$
\text{Loan Face Value} - \text{Disagio} - \text{External Service Costs at } t=0 = \text{Available Funds at } t=0
$$

#### **Cost of Capital (Approximative Yield to Maturity):**
$$
\text{Cost of Capital} = \frac{\sum \text{Total Costs}}{\text{Available Funds at } t=0 \times \text{Mean Time to Maturity}}
$$

#### **Mean Time to Maturity**:
$$
\text{\# periods without repayment} + \frac{\text{\# periods with repayment}+1}{2}
$$


#### **Exact Yield (Internal Rate of Return - IRR)**:
$$
\text{PV} = \sum_{t=1}^{T} \frac{CF(t)}{(1+y)^t}
$$

_Total Costs include: Interest, External Service Costs (ESC), Disagio, Agio._