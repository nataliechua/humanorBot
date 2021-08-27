# # Facebook Recruiting IV: Human or Robot?

This is my entry for the 2015 Kaggle contest held by Facebook, in which participants are challenged to build a machine learning model to predict if an online bid was made by a human or a robot. My model achieved an AUC of 0.8998 on the private leaderboard.

I used ensemble learning with CatBoost and XGBoost, and used the mean of the predictions from these two models for my final prediction. 

Definitely the biggest challenge of the competition was the lack of features, due to how a lot of information such as bidder_id, payment account, address, time and URL were encrypted. Feature engineering was thus crucial to this problem and creativity was needed to maximise the usage of the limited features available.

## Feature Engineering

The final features I ended up including in my model are:
- auction count
- device count
- time count
- country count
- ip count
- url count
- num_bids
- simultaneous countries
- simultaneous devices
- simultaneous auctions
- bids per instant
- bids in an auction
- bids per auction
- bids per device
- bids per ip
- no of first bids
- min delay (minimum delay time between start of auction and time of first bid)
- mean delay (average delay time between start of auction and time of first bid)
- bids per country
- per instant bids (percentage of instantaneous bids)

And the following features which refer to the count of bids placed in each merchandise category:
- auto parts 
- books and music
- clothing
- computers
- furniture
- home goods
- jewelry
- mobile
- office equipment
- sporting goods

## Feature Importance

A quick graph of feature importance gave me more insight into my features and let me know which of them helped my model the most. These happened to be:
- mean delay
- num_bids
- bids per auction
- min delay

This was my first time entering a prediction competition on Kaggle and it proved to be a enjoyable and eye-opening experience! It certainly marks the start of future forays into the boundless world of machine learning and data science, and I look forward to exploring more techniques which can help me enhance my models. 

For more insight into my methodology, please feel free to run my notebook. 

Required data can be found here: https://www.kaggle.com/c/facebook-recruiting-iv-human-or-bot
