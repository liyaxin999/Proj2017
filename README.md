# Proj2017
- Build a generalized linear regression model to do prediction, all the features are selected from LDA.
$$ \log(\frac{Pr[y_{d+1}=1]}{1-Pr[y_{d+1}=1]}) = \beta_0 + \beta_1T_{d,1}+ ...+\beta_kT_{d,k}) $$

- Delta Naive Bayes Model.
  - compute conditional probability matrix $ P(Y|X) $ from $ s_0 = \{(x_{n-L}, y_{n-L}),...,(x_{n-1}, y_{n-1})\}$;
  - compute conditional probability matrix $ Q(Y|X)$ from $ s_0 = \{(x_{n-L+1}, y_{n-L+1}),...,(x_{n}, y_{n})\} $;
  - compute $ \Delta P(Y|X) = abs(Q(Y|X) - P(Y|X))$
  - $ p_{max} = max_{y_j}\Delta P(Y=y_j | X = x_{n+1}) $
  - return $$\hat{y}_{n+1} = arg max_{y_j} \Delta P(Y=y_j | X = x_{n+1})$$ when $p_{max}>t$; 
  otherwise return $\hat{y}_{n+1}$ as "flat"
