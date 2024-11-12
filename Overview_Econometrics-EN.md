title: "Econometrics 1"

subtitle: "Overview"

author: "Tiago Afonso"

description: "This file is only a roadmap for the Econometrics course. It contains the main topics and concepts that was covered during the course. This guide is not comprehensive enough to fully understand the subject. It is recommended 
to use this file as a complement to the course materials."

date: "11/11/2024"

keywords: Econometrics; Linear Models; Generalized Linear Models;

# Econometrics Overview

## 1 Data types and data structures

### 1.1 Data structures

-   **sectional data**: data collected at a single point in time

-   **time series data**: data collected over time

-   **pane data**: data collected over time and cross-sectional units

-   **spatial data**: data collected over space (e.g. geographical data)

### 1.2 Data transformations

-   **logarithm transformation**: $ \color{purple}y = \log(x)$
-   **percentage change**: $\color{purple}\frac{y_t - y_{t-1}}{y_{t-1}}$
-   **difference**: $\color{purple}y_t - y\_{t-1}$
-   **per capita**: $\color{purple}\frac{y}{pop}$
-   **inverted**: $\color{purple}\frac{1}{y}$
-   **lag**: $\color{purple}y\_{t-1}$
-   **square**: $\color{purple}y_{sq}=y^2$

### 1.3 Data types

-   **continuous**: e.g. income, age
-   **discrete**: e.g. number of children
-   **binary**: e.g. approved or not approved
-   **ordinal**: e.g. education level
-   **nominal**: e.g. country name
-   **time**: e.g. date, time
-   **geographical**: e.g. latitude, longitude
-   **muultinomial**: e.g. political party, or car color

### 1.4 Data sources

-   **primary data**: data collected by the researcher
-   **secondary data**: data collected by someone else
-   **administrative data**: data collected by government or other organizations
-   **big data**: large and complex data sets
-   **open data**: data that is freely available to everyone
-   **proprietary data**: data that is owned by a company or organization

### 1.5 Variables - tests

-   **normality test**: test if the data is normally distributed; e.g. *histrogram*; *Shapiro-Wilk test*; *Jarque-Bera test*; (skewness and kurtosis)
-   **variability coefficient**: standard deviation/mean;

## 2 Linear regression models

### 2.1 Simple linear regression and multiple linear regression
-   **Purpose**: Used for estimating the relationship between a dependent variable and one ot more independent variables.
-   **Method**: OLS - Minimizes the sum of squared residuals.
-   **Dependent Variable**: Continuous

-   **Equations**:
        - Simple regression: $\color{purple}y = \beta_0 + \beta_1 x + u$
        - Multiple regression: $\color{purple}y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_k x_k + u$
        Where: $\color{purple}y$ is the dependent variable, $\color{purple}x$ is the independent variable, $\color{purple}\beta_0$ is the intercept, $\color{purple}\beta_1...\beta_k$ are the coefficients of the independent variables, $\color{purple}u$ is the error term.

#### 2.1.1 Assumptions

-   **normality**: errors are normally distributed
-   **linearity**: the relationship between the dependent and independent variables is linear
-   **homoscedasticity**: constant variance of errors. e.g. *white test*; *ARCH test*; *Park test*...
-   **independence**: observations are independent of each other. e.g. No serial correlation between erros.
-   **no multicollinearity**: independent variables are not highly correlated with each other. e.g. *VIF test*; *correlation matrix*; *plot*; *regressions*...

#### 2.1.2 Model fit - goodness of fit

-   **R-squared**: the proportion of variance in the dependent variable that is explained by the independent variables.
-   **Adjusted R-squared**: a modified version of R-squared that adjusts for the number of independent variables in the model.

#### 2.1.3 Interpretation

-   **Coefficients**: represent the change in the dependent variable for a one-unit change in the independent variable. It dependes on the scale of the independent variable and model specification.

#### 2.1.4 Hipothesis testing

-   **individual coefficients**: test the significance of each coefficient. *t-test*
-   **linear combination of coefficients**: test the significance of a linear combination of coefficients. *F-test*
-   **overall model**: test the overall significance of the model. *F-test*

#### 2.1.5 Generalized Least Squares - GLS

#### 2.1.6 Weighted Least Squares - WLS

## 3. Model evaluation (OLS)

-   **F-test**: joint significance of the independent variables
-   **t-test**: significance of individual coefficients
-   **R-squared/adjusted R-squared**: goodness of fit
-   **Information criteria**: AIC, BIC, HQIC
-   **residual tests:**: normality test (Jarque-Bera), heteroskedasticity.
-   **tests for strucuture**: Ramsey RESET test (miss specification - functional funcional), Chow test (structural break in the model), CUSUM and CUSUMSQ tests (coefficients stability)
-   **redundant variable test**: likelihood ratio test
-   **omitted variable test**: likelihod ratio test
-   **multicollinearity test**: VIF, regressions

## 4. Some extensions

-   seasonality
    -   detection:
        -   plot
        -   regression
    -   dealing with:
        -   seasonal dummies
        -   seasonal adjustment - stl decomposition
        -   homologous series
-   dummy variables:
    -   impulse
    -   shift
    -   seasonal

## 5. Limited dependent variable model (binary choice model)

-   **Purpose**: Used for modeling binary outcome variables.
-   **Dependent Variable**: Binary (0 or 1).

### LPM - linear probability model

-   **method**: OLS
    -   **interpretation**: Coefficients represent the change in the probability of the dependent variable for a one-unit change in the independent variable. **Predict the probability of success (when d=1)**
    -   **assumptions**:
        -   **linearity**: the relationship between the dependent and independent variables is linear
        -   **homoscedasticity**
        -   **independence**
        -   **normality**
-   **main limitation**: predicted probabilities can be outside the [0,1] range.
-   **percentage correctly predicted**: the proportion of observations that are correctly predicted by the model (nº of times that $y=\hat{y}$)
-   **solution**: use the logit or probit model.


### Logit and Probit Model

-   **method**: *Maximum likelihood estimation* - ("Método da máxima verossimilhança")
-   **assumption**: linearity in logit (log odds) or probit (z-score)
-   **ouptut**: signal and stattistical significance of the coefficients
-   **inetrpretation**: partial effect at mean or average partial effect
-   **Predict the probability of success (when d=1)**

#### Model fit

-   **pseudo R-squared**: a measure of the goodness of fit of the model.
-   **likelihood ratio test**: compares the fit of the model to a null model (only with intercept).
-   **percentage correctly predicted**: the proportion of observations that are correctly predicted by the model (nº of times that d=d_hat)

### Tobit model

-   **method**: *Maximum likelihood estimation*
-   **definition**: used when the dependent variable is censored or truncated. e.g. income, prices, index of happiness; e.g. *censoring*: when the dependent variable is observed only if it is above or below a certain threshold (variables outside the threshold assume the values of the threshold) ; e.g. *truncation*: when the dependent variable is observed only if it is below or above a certain threshold (valued removed).

## 6. Spatial models (spatial econometrics)

Definition: models that account for the spatial relationships between observations.