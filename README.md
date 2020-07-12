
# 아래 링크를 누르시고 핸즈온 사전 단계를 진행 해주세요.(This is a Prerequisite Step for later Contents)

[핸즈온 준비 필수 단게: Prerequisite](0.0.Prerequisite/Prerequisite.md)

**Prerequisite Task: Make sure that a role for SageMaker notebook instance has these policies attached such as AmazonSageMakerFullAccess, AmazonS3FullAccess, AmazonForecastFullAccess, IAMFullAccess**

## 

## Forecasting Store Item Demanding with AWS Forecast  
(Data Source: https://www.kaggle.com/c/demand-forecasting-kernels-only/overview)

* **Description: Using AWS Forecast AI, forecasting the store item demanding problem (Daily Data)**

* **Technique included**
    * Use two dimenstions, item_id and store on Target Data
    * Use QueryForecast with two filters, item_id and store
    * Use QueryForecast with one filters, item_id 
    * Use HPO for building DeepARP 
    * Measure MAPE on Prophet and Deeparp campaigns    
    * Compare Prophet and DeepARP performance with actual value

## 아래 단계에서 1~6번까지의 노트북을 실행 하시면 됩니다.

* Process: (In the folder StoreItemDemand, run the following notebooks in order)
    * 1.Prepare_Data_File.ipynb
        
        * Prepare data file handling a raw data file
        
    * 1.1. Generate Related Time Series 
    
        * Prepare data file for Related Time series
    
    * 2.Import_Dataset.ipynb (About 10 mins elapsed)
        * Create dataset group, dataset and dataset import job as well as importing the data file from S3
        * The dataset file as target time series data has two dimensions such as item_id and store
        
    * 
    
    * 3.Create_Target_Predictors.ipynb (About 40 mins elapsed)
        
        * Create predictors with the prophet and deepar+ 
        
    * 4.Create_Target_Forecast.ipynb (About 50 mins elapsed)
        
        * Create forecasts with the two predictors 
        
    * 5.Analyze_Target_Forecast.ipynb (About 10 mins elapsed)
        
        * Analyze results on the forecasts
        
    * 6.Cleanup.ipynb (About 10 mins elapsed)
        
        * Clean up resources
        
    * 7.Option_Create_Target_Predictors_HPO.ipynb (About 90 mins elapsed)
        * Turning on HPO option, create  a predictor with deepar+ 
          
          
