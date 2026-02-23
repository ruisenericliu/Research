Example ML Systems and LifeCycles
 
Autonomous Vehicles:
 
Data ingestion -- \> Data curation --\> Data labeling --\> Data prep --\> Model training --\> Model validation --\> System Development --\> Offline & Online Validation --\> Production deployment --\> Telemetry & Log Data --\> Data ingestion
 
Over 50% effort is on data. Much Validation needed
 
Retail Recommendations:
 
Live Data --\> Production inference --\> Predictions + Metrics Database ￼  
Production training and experimental data science are separate  
￼Production inference : Retrieval --\> Filtering (business tool) -- Scoring --\> Ordering
 
Each component is a separate piece of software
 
Special considerations:

1. Privacy-preserving and distributed training
2. Explainablity
3. Inference for LLMS and Generative AI --\>
 
Defining ML Ops, Revisited
 
1. Sculley et al. "hidden Technical Debt in Machine Learning Systems, NIPS 2015"
2. Most people who say they do ML Ops, they focus on serving infrastructure
3. ![Exported image](Exported%20image%2020260222202325-0.png)
    
How does the ML Ops support these subsystems?
      

Roles:
 ![Exported image](Exported%20image%2020260222202327-1.png)     
![Exported image](Exported%20image%2020260222202328-2.png)   
Recommendations:
   
![Exported image](Exported%20image%2020260222202330-3.png)   
Permutations and selection -- automated process for pushing

![Exported image](Exported%20image%2020260222202333-4.png)  
![Exported image](Exported%20image%2020260222202334-5.png)     
![Exported image](Exported%20image%2020260222202335-6.png)   ![Exported image](Exported%20image%2020260222202336-7.png)  
![Exported image](Exported%20image%2020260222202341-8.png)  
![Exported image](Exported%20image%2020260222202342-9.png)     
![Exported image](Exported%20image%2020260222202343-10.png)     
![Exported image](Exported%20image%2020260222202345-11.png)  
![Exported image](Exported%20image%2020260222202346-12.png)   ![Exported image](Exported%20image%2020260222202347-13.png)