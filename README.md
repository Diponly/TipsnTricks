# TipsnTricks

how to win a ML competition ?

Steps: 

Data -> Model -> Submission -> Evaluation -> Leaderboard


kaggle , DrivenData, CrowdAnalityx,Codelab,DatascienceChallenge.net,
Datascience.net,
Singlw-Competition sites like(KDD,VizDooM)

Understanding of business problem
Problem Formalization
Data Collection
Data Preprocessing
Modelling
Way to evaluate model in real life
Way to deploy model

Preprocessing :- 

>>>>>  Numeric Data  feature preprocessing : - 
   [[ a . Tree based models doesn't depend on scaling
      b . Non Tree based models hugely depend on scaling
   ]]

  1 > Scaling (MinMaxScaler,StandardScaler)
  2 > Clipping to handle outlier 
          [UPPERBOUNF,LOWERBOUND = np.percentile(x,[1,99])
          y = np.clip(x,UPPERBOUND,LOWERBOUND)
          pd.Series(y).hist(bins=30
          
  3 > Ranking also to handle outlier
          [scipy.stats.rankdata
           rank([-100,0,1e5]) == [0,1,2]
           ]
           
  4 > Log Trasform [ np.log(1 + x) ] - This makes value near 0 more distinguishable
  5 > Raising to power < 1 [ np.sqrt(x+2/3) ] 
  
  Numeric Data Feature generation :
   
   1 > Combine feature to derive new features.
   2 > fractional part generation 
   
>>>>>  Categorical Data  feature preprocessing : - 

Label Encoding - sklearn.preprocessing.LabelEncoder [S,C,Q] -> [2,1,3]
               - pandas.factorize [S.C.Q] - [1,2,3]
               
Frequency Encoding - [[ encoding = titanic.groupby('Embarked').size()
                        encoding = encoding/len(titanic)
                        titanic['enc'] = titanic.Embarked.map(encoding)
                      ]]
                      
                   - from scipy.stats import rankdata
Onehot encoding - pandas.get_dummies
                  sklearn.preprocessing.OneHotEncoding
                  
                      
  
