## Overview: Comparing OLS with Logit and Probit

### Ordinary Least Squares (OLS)
- **Purpose**: Used for estimating the relationships between a dependent variable and one or more independent variables.
- **Dependent Variable**: Continuous.
- **Model**: Linear regression model.
- **Assumptions**:
    - Linearity: The relationship between the dependent and independent variables is linear.
    - Homoscedasticity: Constant variance of errors.
    - Independence: Observations are independent of each other.
    - Normality: Errors are normally distributed.
- **Estimation**: Minimizes the sum of squared residuals.
- **Interpretation**: Coefficients represent the change in the dependent variable for a one-unit change in the independent variable.

### Logit Model
- **Purpose**: Used for modeling binary outcome variables.
- **Dependent Variable**: Binary (0 or 1).
- **Model**: Logistic regression model.
- **Assumptions**:
    - Linearity in the logit: The log odds of the dependent variable are a linear combination of the independent variables.
    - Independence: Observations are independent.
- **Estimation**: Maximum likelihood estimation.
- **Interpretation**: Coefficients represent the change in the log odds of the dependent variable for a one-unit change in the independent variable.

### Probit Model
- **Purpose**: Also used for modeling binary outcome variables.
- **Dependent Variable**: Binary (0 or 1).
- **Model**: Probit regression model.
- **Assumptions**:
    - Linearity in the probit: The probit (inverse of the cumulative distribution function of the standard normal distribution) of the dependent variable is a linear combination of the independent variables.
    - Independence: Observations are independent.
- **Estimation**: Maximum likelihood estimation.
- **Interpretation**: Coefficients represent the change in the probit (z-score) of the dependent variable for a one-unit change in the independent variable.

### Key Differences
- **Dependent Variable**: OLS is for continuous outcomes, while Logit and Probit are for binary outcomes.
- **Model Type**: OLS uses a linear model, Logit uses a logistic model, and Probit uses a probit model.
- **Estimation Method**: OLS uses least squares, while Logit and Probit use maximum likelihood estimation.
- **Interpretation**: OLS coefficients are changes in the dependent variable, Logit coefficients are changes in log odds, and Probit coefficients are changes in z-scores.

### Conclusion
OLS is suitable for continuous dependent variables, while Logit and Probit are appropriate for binary dependent variables. The choice between Logit and Probit often depends on the specific application and preference for interpretation.
