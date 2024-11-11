- title: "Econometrics Overview"

# Econometrics Overview

## 1. Data types and data structures

### Data strucutres

-   **sectional data**: data collected at a single point in time

-   **time series data**: data collected over time

-   **pane data**: data collected over time and cross-sectional units

-   **spatial data**: data collected over space (e.g. geographical data)

### Data transformations

-   **logarithm transformation**: (y = \log(x))
-   **percentage change**: (\frac{y_t - y_{t-1}}{y_{t-1}})
-   **difference**: (y_t - y\_{t-1})
-   **per capita**: (\frac{y}{pop})
-   **inverted**: (\frac{1}{y})
-   **lag**: (y\_{t-1})
-   **square**: (y\^2)

### Data types

-   **continuous**: e.g. income, age
-   **discrete**: e.g. number of children
-   **binary**: e.g. approved or not approved
-   **ordinal**: e.g. education level
-   **nominal**: e.g. country name
-   **time**: e.g. date, time
-   **geographical**: e.g. latitude, longitude
-   **muultinomial**: e.g. political party, or car color

### Data sources

-   **primary data**: data collected by the researcher
-   **secondary data**: data collected by someone else
-   **administrative data**: data collected by government or other organizations
-   **big data**: large and complex data sets
-   **open data**: data that is freely available to everyone
-   **proprietary data**: data that is owned by a company or organization

### Variables - tests

-   **normality test**: test if the data is normally distributed; e.g. *histrogram*; *Shapiro-Wilk test*; *Jarque-Bera test*; (skewness and kurtosis)
-   **variability coefficient**: standard deviation/mean;

## 2. Linear regression

### Simple linear regression and multiple linear regression

-   **Purpose**: Used for estimating the relationship between a dependent variable and one ot more independent variables.
-   **method**: OLS - Minimizes the sum of squared residuals.
-   **Dependent Variable**: Continuous

#### Assumptions

-   **normality**: errors are normally distributed
-   **linearity**: the relationship between the dependent and independent variables is linear
-   **homoscedasticity**: constant variance of errors. e.g. *white test*; *ARCH test*; *Park test*...
-   **independence**: observations are independent of each other. e.g. No serial correlation between erros.
-   **no multicollinearity**: independent variables are not highly correlated with each other. e.g. *VIF test*; *correlation matrix*; *plot*; *regressions*...

#### Model fit - goodness of fit

-   **R-squared**: the proportion of variance in the dependent variable that is explained by the independent variables.
-   **Adjusted R-squared**: a modified version of R-squared that adjusts for the number of independent variables in the model.

#### Interpretation

-   **Coefficients**: represent the change in the dependent variable for a one-unit change in the independent variable.

#### Hipothesis testing

-   **individual coefficients**: test the significance of each coefficient. *t-test*
-   **linear combination of coefficients**: test the significance of a linear combination of coefficients. *F-test*
-   **overall model**: test the overall significance of the model. *F-test*

##### Generalized Least Squares - GLS

##### Weighted Least Squares - WLS

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
    -   detection
        -   plot
        -   regression
    -   dealing with
        -   seasonal dummies
        -   seasonal adjustment - stl decomposition
        -   homologous series
-   dummy variables
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
-   **main limitation**: predicted probabilities can be outside the \[0,1\] range.
-   **percentage correctly predicted**: the proportion of observations that are correctly predicted by the model (nº of times that d=d_hat)
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
-   **definição**: usado quando a variável dependente é censurada ou truncada. e.g. rendimento, preços, índice de felicidade; e.g. *censura*: quando a variável dependente é observada apenas se estiver acima ou abaixo de um certo limite (valores são registados mas assumed o valor do limte); e.g. *truncados*: quando a variável dependente é observada apenas se estiver abaixo ou acima de um certo limite (valores fora do limite são removidos da amostra).

## 6. Spatial models (spatial econometrics)

Definition: models that account for the spatial relationships between observations. e.g. spatial autocorrelation, spatial heterogeneity, spatial dependence.