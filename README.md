# Proj2017
- Build a generalized linear regression model to do prediction, all the features are selected from LDA.
$$ \log(\frac{Pr[y_{d+1}=1]}{1-Pr[y_{d+1}=1]})%20=%20\beta_0%20+%20\beta_1T_{d,1}+%20...+\beta_kT_{d,k}) $$

- $ T_{d,k} $ is LDA's k th feature from day d. $ y_{d+1} $ is  prediction results of day d+1

- return 

$$ \hat{y}_{n+1}  $$

when $p_{max}>t$; 

otherwise return $\hat{y}_{n+1}$ as "flat"
