# Fund-Raising-Prediction---Direct-Marketing-to-PVA-Donors

This project is aimed to analyze the consequence of a direct marketing project provided by the Paralyzed Veterans of America (PVA). While the original objective for this challenge is to maximize the profit, to make it simple, I was asked to focus on developing a predictive model to identify top responders. In other words, This project is to develop a predictive model to predict dependent variable ‘Target_B’, and find relevant factors associated with donation behavior.

To explore more background informaton: http://www.kdd.org/kdd-cup/view/kdd-cup-1998/Tasks

Data file path: http://www.kdd.org/kdd-cup/view/kdd-cup-1998/Data   
     # cup98lrn.zip PKZIP compressed raw LEARNING data set. (36.5M; 117.2M uncompressed)   
     # cup98val.zip PKZIP compressed raw VALIDATION data set. (36.8M; 117.9M uncompressed)     
     # cup98dic.txt. Data dictionary to accompany the analysis data set   
 

![#1589F0](https://placehold.it/15/1589F0/000000?text=+) `Find code file:` PVA .ipynb


Data Preparation:   
1.1 load dataset     
1.2 target distribution     
       # only 5.07% donors respond     
1.3 encode data into numerics      
       # using label encoder to encode 74 string columns into numerics     
1.4 feature selection     
       # using ExtraTreesClassifier to reduce dimensions from 480 to 17     
1.5 oversampling      
       # using naive resample approach to rebalance data into 70/30     
1.6 data partition          
       # df_train 70%      
       # df_val   30%     
       
Model:    
2.1 Logistic Regression          
       # Train data Pseudo R-squ.:  0.5476     
       # Test  data Pseudo R-squ.:  0.5427     
       # Top responders: RFA_2, RFA_2R, RFA_2F      

2.2 Decision Tree     

![alt text](https://github.com/versehe/Fund-Raising-Prediction---Direct-Marketing-to-PVA-Donors/blob/master/Capture2.PNG?raw=true)    
       *To see whole tree: copy code in 'tree.dot' file and paste it to http://webgraphviz.com/                  
       
 2.3 Random Forrest      
       # Train data R-2 score: 0.999963703252    
       # Test data R-2 score: 0.999682054237     
       # Top responders:    
       ![alt text](https://github.com/versehe/Fund-Raising-Prediction---Direct-Marketing-to-PVA-Donors/blob/master/Capture.PNG?raw=true)    
        
       
             
        
        

       
Results:    
RFA Status: RFA_2 , RFA_2R, RFA_2F
![alt text](https://github.com/versehe/Fund-Raising-Prediction---Direct-Marketing-to-PVA-Donors/blob/master/Capture_RFA.PNG?raw=true)
Donors Neighborhood: POP903, POP901
![alt text](https://github.com/versehe/Fund-Raising-Prediction---Direct-Marketing-to-PVA-Donors/blob/master/Capturepop.PNG?raw=true)
Donors Giving History: LASTDATE, MAXRDATE, NEXTDATE, TIMELAG
![alt text](https://github.com/versehe/Fund-Raising-Prediction---Direct-Marketing-to-PVA-Donors/blob/master/Capture_date.PNG?raw=true)
       

       
       
       

       
       
       

       

       
 
       

       
       
       









 


