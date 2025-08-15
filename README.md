# Real Estate Investment Profitability Calculator

A ML-powered tool for evaluating real estate investment opportunities. This calculator uses ML models trained on actual housing market data to predict property values, estimate rental income, and calculate key investment metrics.

## What It Does

This tool analyzes real estate investment opportunities by:

**Property Valuation**: Uses Random Forest, Gradient Boosting, and Linear Regression models to predict property values based on features like square footage, bedrooms, bathrooms, location, and property condition.

**Investment Analysis**: Calculates essential investment metrics including Cash-on-Cash Return, Cap Rate, Gross Yield, and generates an ML-enhanced risk score for each property.

**Rental Income Estimation**: Automatically estimates expected rental income based on property characteristics and local market data.

**Risk Assessment**: Evaluates investment risk by analyzing property age, condition, cash flow potential, and market pricing relative to local averages.

**Long-term Projections**: Forecasts investment performance over 10 years, including property value appreciation and cumulative cash flow.

**Property Comparison**: Allows side-by-side analysis of multiple investment opportunities with visual comparisons of key metrics.

**Market Segmentation**: Automatically categorizes properties into market segments (Budget, Mid-Range, Premium, Luxury) using clustering analysis.

## Key Features

- Loads and preprocesses data from a housing CSV file
- Trains and compares multiple machine learning models for property valuation
- Engineers  features like price per square foot, property age, and lot ratios
- Calculates financing scenarios with customizable down payment and loan terms
- Provides automated investment recommendations based on calculated metrics
- Generates comprehensive visualizations of model performance and investment analysis
- Includes customizable analysis section for evaluating specific properties

## How Investment Metrics Are Calculated

**Cash-on-Cash Return**: Annual cash flow divided by total cash invested. Measures the return on actual cash invested.

**Cap Rate**: Net operating income divided by property value. Shows the property's return potential independent of financing.

**Risk Score**: ML-generated score (0-10) considering property age, condition, cash flow potential, and market factors.

**Gross Yield**: Annual rental income divided by property value. Basic measure of rental income relative to property cost.

# Real Estate Investment Profitability Calculator

A machine learning-powered tool for evaluating real estate investment opportunities. This calculator uses ML models trained on actual housing market data to predict property values, estimate rental income, and calculate key investment metrics.

## What It Does

This tool analyzes real estate investment opportunities by:

**Property Valuation**: Uses Random Forest, Gradient Boosting, and Linear Regression models to predict property values based on features like square footage, bedrooms, bathrooms, location, and property condition.

**Investment Analysis**: Calculates essential investment metrics including Cash-on-Cash Return, Cap Rate, Gross Yield, and generates an ML-enhanced risk score for each property.

**Rental Income Estimation**: Automatically estimates expected rental income based on property characteristics and local market data.

**Risk Assessment**: Evaluates investment risk by analyzing property age, condition, cash flow potential, and market pricing relative to local averages.

**Long-term Projections**: Forecasts investment performance over 10 years, including property value appreciation and cumulative cash flow.

**Property Comparison**: Allows side-by-side analysis of multiple investment opportunities with visual comparisons of key metrics.

**Market Segmentation**: Automatically categorizes properties into market segments (Budget, Mid-Range, Premium, Luxury) using clustering analysis.

## Key Features

- Loads and preprocesses housing market data from CSV files
- Trains and compares multiple machine learning models for property valuation
- Engineers relevant features like price per square foot, property age, and lot ratios
- Calculates financing scenarios with customizable down payment and loan terms
- Provides automated investment recommendations based on calculated metrics
- Generates comprehensive visualizations of model performance and investment analysis
- Includes customizable analysis section for evaluating specific properties

## How Investment Metrics Are Calculated

**Cash-on-Cash Return**: Annual cash flow divided by total cash invested. Measures the return on actual cash invested.

**Cap Rate**: Net operating income divided by property value. Shows the property's return potential independent of financing.

**Risk Score**: ML-generated score (0-10) considering property age, condition, cash flow potential, and market factors.

**Gross Yield**: Annual rental income divided by property value. Basic measure of rental income relative to property cost.

## How to Customize for Your Property

To analyze your own property, modify Section 11 of the notebook by updating the `your_property_features` dictionary with your property's details:

```python
your_property_features = {
    # Property characteristics
    "bedrooms": 3,
    "bathrooms": 2.5,
    "sqft_living": 2000,
    "sqft_lot": 8000,
    "floors": 2,
    "waterfront": 0,  # 1 if waterfront, 0 if not
    "view": 1,        # 0-4 scale
    "condition": 4,   # 1-5 scale
    "property_age": 15,
    
    # Financial parameters
    "purchase_price": 400000,     # Optional: specify price or let ML predict
    "down_payment_pct": 20,       # Percentage down payment
    "loan_rate": 6.5,             # Annual interest rate
    "monthly_rent": 2800,         # Optional: specify rent or let ML estimate
    "annual_appreciation": 3.5,   # Expected annual appreciation rate
    "annual_expenses_pct": 25,    # Operating expenses as % of rental income
    "vacancy_rate": 5,            # Expected vacancy rate percentage
    "analysis_years": 10          # Years to project returns
}
```

**Customization Options:**

- **Automatic vs Manual Input**: Leave out `purchase_price` to use ML prediction, or include it to use your own valuation. Same applies to `monthly_rent`.

- **Financing Terms**: Adjust `down_payment_pct` and `loan_rate` to match your financing options.

- **Market Assumptions**: Modify `annual_appreciation`, `annual_expenses_pct`, and `vacancy_rate` based on your local market knowledge.

- **Analysis Period**: Change `analysis_years` to project returns over your preferred time horizon.

- **Property Comparison**: Add multiple properties to the `properties_to_compare` list in Section 10 to analyze several opportunities simultaneously.

After updating your property details, run the notebook cells to get customized analysis including ML-predicted values, investment metrics, risk assessment, and long-term projections specific to your property.