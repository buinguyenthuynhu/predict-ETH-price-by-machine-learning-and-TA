# predict-ETH-price-by-machine-learning-and-TA
Applying technical analysis and machine learning to predict the price trend of Ethereum

CHAPTER 1: INTRODUCTION

1.1 The research context

In the context of the Industrial Revolution 4.0, which is developing strongly around the world in general and in Vietnam in particular. Thanks to the achievements from the Industrial Revolution 4.0 such as machine learning, cloud computing, artificial intelligence, etc., which continuously develop and breakthrough, humans have successfully applied those techniques to various fields in the world. life and typically in financial investment. In particular, machine learning is an effective assistant in the field of investment forecasting and recommendation.

Digital currency is becoming a new investment craze as these cryptocurrencies are growing in both market share and market value. Cryptocurrency trading has also become easy and popular in Vietnam.

The digital currency revolution began with the emergence of cryptocurrency, leading to a new era of the digital age, with the emergence of this currency having a strong influence on the current financial market. in. It is even unpretentious that many researchers believe that the global financial market has completely changed when trillions of dollars have been allocated to the next-generation digital currency market, financial transactions are free. Automated by pre-programmed code, a world where all assets are digitized and anonymous, markets are no longer controlled but decentralized with stakeholder contributions. market.
With such great features and advantages, in recent years we have witnessed the tremendous growth of the cryptocurrency market. Definitely, Ethereum - a coin that has grown strongly since 2017, by market capitalization just behind Bitcoin, occupies the 2nd position in the market.
The reason why many investors are interested in Ethereum compared to other coins, especially Bitcoin is that Ethereum and Bitcoin are both digital currencies, but in general their purposes are different. The characteristic of Ethereum is that this coin is not designed as an alternative payment solution, but rather to promote developers to create and operate applications in the Ethereum network.

Ethereum allows the exchange of money and assets quickly and much more cost-effectively than having to depend on an intermediary chain. Ethereum is even more appreciated than Bitcoin because Ethereum is more than just a cryptocurrency. Moreover, the Ethereum network also helps to create online marketplaces and programmable transactions known as smart contracts.

Ethereum with its huge potential and ecosystem has attracted investors, especially those who are new to the market. These advantages also make Ethereum more potential than ever and push the price of Ethereum up.

1.2 Urgency of the topic

With the topic "Applying technical analysis and machine learning to predict the price trend of Etherium", the author expects the research paper to have scholarly value as follows:

Firstly, research is exploration, learning and collaboration of short-term price trend forecasting models suitable for Etherium. This contributes to a more complete reflection, as well as a more sophisticated algorithmic setup.

Secondly, this study once again confirms the conclusion that the past price has a strong impact on the movement of Etherium in the short term, and from that, it is recommended that investors pay attention to the influence of price in the short term. past to present.

Along with the academic values, the study also has the following practical significance:
Realizing the need to invest from idle cash flows and the difficulties that investors face, especially As new and inexperienced investors, research is expected to be an effective support tool, helping investors make accurate decisions at each time. From there, the author wishes the tool will reduce the risk of losing money and help investors have more income from their idle cash flow. There is no denying the current attraction of cryptocurrencies in general and Ethereum in particular to investors when the total cryptocurrency market capitalization currently reaches more than 2 trillion USD (according to coinmarketcap.com). 	 

1.3 Research objectives and research scope
1.3.1 Research objectives
 The objectives of the research paper include the following:
- Machine learning algorithms using input variables as indicators from technical analysis method
- The efficiency of the prediction algorithms and model compared to the actual data.
1.3.2 Research scope
Spatial scope: The study uses secondary data which is historical price including: high price, low price, opening price, closing price, adj closing price and trade volume of Etherium is taken from finance.yahoo.com database.
Time range: The data set is taken from the securities codes traded for the first time Etherium is traded to June 17, 2022. This is the best time period, with limited empty data and enough background data for the study.

CHAPTER 2: PROCESS

![image](https://user-images.githubusercontent.com/118440399/202441979-b020ee87-83dc-4277-9a41-b8682f8bcef9.png)

CHAPTER 3: RESULTS

3.1 Random Forest Model
 
![image](https://user-images.githubusercontent.com/118440399/202442520-03c071aa-3b4d-4408-bf21-4add3dc9ed79.png)


The n_estimators for the highest model performance is 140
The accuracy of model is quite high: 83%. However, the limitation of accuracy is measuring on all labels without caring about the accuracy on each label. Therefore, it is not suitable for evaluating tasks where the importance of predicting different labels must be focused. Specifically:
•	The model correctly predicted 161 cases of decreased/unchanged and actual decreased/unchanged 
•	Model just only misses 22 cases actual increase
•	The model correctly predicted 185 cases of increase and actual increase
•	The model incorrectly predicted 47 cases actual decreased/unchanged.
•	The precision good predicts class "Decreased": 88% and quite good predicts class " Increased ": 80%.
•	The recall good predicts class " Increased ": 89% and quite good predicts class "Decreased": 77%.
•	Both precision and recall are good so this is a good predictive model.

![image](https://user-images.githubusercontent.com/118440399/202442598-12c5cea7-1cf5-4f1a-a177-51e661a8c5c6.png)


With the above results, it can be seen that the variable "20 period CCI" has the most branching significance with Feature Importance more than 80%, followed by the variable "14 period ATR" with a value of about 80%, and finally the variable "MOM" with a value of more than 70%. It can be said that these three variables represent momentum and volatility indicator that affect the model the most

3.2 K-Nearest Neighbors Model

![image](https://user-images.githubusercontent.com/118440399/202442695-b7fc9078-d46b-416b-8bc0-e11c09c890fb.png)


The n_neighbors for the highest model performance is 1
The accuracy of model is slightly high: 80%. However, the limitation of accuracy is measuring on all labels without caring about the accuracy on each label. Therefore, it is not suitable for evaluating tasks where the importance of predicting different labels must be focused. Specifically:
•	The model correctly predicted 159 cases of decreased/unchanged and actual decreased/unchanged 
•	Model just only misses 35 cases actual increase
•	The model correctly predicted 172 cases of increase and actual increase
•	The model incorrectly predicted 49 cases actual decreased/unchanged.
•	The precision good predicts class "Decreased": 82% and quite good predicts class " Increased ": 78%.
•	The recall good predicts class " Increased ": 83% and quite good predicts class "Decreased": 76%.
•	Both precision and recall are good so this is a good predictive model

3.3 Ensemble Model

![image](https://user-images.githubusercontent.com/118440399/202444076-74856cf3-521d-4a39-877f-a744d1f2eb33.png)

The accuracy of model is higher than previous model: 84%. However, the limitation of accuracy is measuring on all labels without caring about the accuracy on each label. Therefore, it is not suitable for evaluating tasks where the importance of predicting different labels must be focused. Specifically:
•	The model correctly predicted 182 cases of decreased/unchanged and actual decreased/unchanged 
•	Model just only misses 42 cases actual increase
•	The model correctly predicted 65 cases of increase and actual increase
•	The model incorrectly predicted 26 cases actual decreased/unchanged.
•	The precision quite good predicts class "Decreased": 81% and very good predicts class " Increased ": 86%.
•	The recall very good predicts class " Increased ": 88% and quite good predicts class "Decreased": 80%.
•	Both precision and recall are good so this is a good predictive model
It can be said, based on the accuracy and precision of the increasing case, in order to find the optimal profit for investors. Precison of the variable "Increased" is 86%, a very high rate that can be trusted by investors and make appropriate investment recommendations from time to time.

CHAPTER 4: CONCLUSIONS AND RECOMMENDATIONS

4.1 Conclusions and limitations

4.1.1 Conclusions

The study aims to create a predictive model from synthetic algorithms based on machine learning and the theoretical basis of Technical Analysis on the Vietnamese stock market, from which the model will provide tools suggesting investment decisions to help investors choose options to buy or sell, in order to increase investment efficiency. To build the model, the authors used support packages available in Python, technical analysis indicators, then used the method of grouping companies and handling these groups and included it in the Model. Random Forest taxonomy. And from this synthetic model, in general, the study has some conclusions as follows:
- Firstly, it can be concluded that the past price has a strong impact on the performance of Ethereum in the short term, and it is recommended that investors pay attention to the influence of the past price to the present.
- Second, with Ensemble Model, the accuracy is 84% and precision is 86%, a high rate.
- Third, the predictive model with technical variables used in this study is more suitable for short-term forecasting than for long-term forecasting.
- Finally, the predictive model can be seen as a tool to help investors refer to it with a reliable level from which to determine when to invest and earn profits for themselves.

5.1.2 Limitations

Although the research paper gives positive results, under the objective influences, the topic still has some incomplete problems, the study still has limitations such as the number of observations is quite small compared to the number of observations that I desire. Other classification models have not been tested for better results. This also will be the one motivation to continue to improve the topic to move forward to further 

5.2 Recommendations 

In the future, to continue the development of this study, there are many plans to incubate as follows:  
The Ethereum forecast analysis problem is only based on closing price data and technical indicators, so it is not a good idea to evaluate the whole picture of the model. For accurate analysis and prediction, it is necessary to rely on a larger number of variables and exclude inflation for more accurate analysis and forecast.
Moreover, in forecasting, it is recommended to use a combination of models, because each model has a different advantage in the forecasting process and the results of each model will play a supporting and testing role for each model. remaining model. Therefore, in the future, it is recommended to use more deep learning models such as LSTM or RNN to combine to produce the most accurate prediction.
In summary, the purpose of the study is to provide a model for investors to refer to. Certainly, the study still has many points to improve in terms of the model, or there may be some errors in the code or some other hidden errors that the author has not discovered or completely fixed. The data also cannot be obtained because Ethereum is still a new coin and there is no complete data. Finally, the author will try to overcome the weaknesses, try different methods of model completion and time series prediction.

