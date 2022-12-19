# NFT_Buy

---

## Project 2 - "Happy Monkey" Automated NFT Trading Bot

NFTs have become quite popular in recent memory. They are still a lucrative market, one that is highly nuanced and tricky to gauge. In an attempt to begin to make sense of this market, we have developed the "Happy Monkey" Automated NFT Trading Bot. The bot serves a client, a potential NFT investor, who is interested in identifying the most traded collections of the day and using their ETH to purchase/sell collections based on market movement. 

This repository houses the chatbot functionality which relays directly with the potential NFT investor. The API data pull, Supervised Learning practices, and algorithm, regression, and trading results are all housed within this repository as well. Continue reading for an overview of how to use the Happy Monkey Automated NFT Trading Bot. 

---

## Technologies

This program uses the following programs and pacakges:  
Python version 3.9.15  
python-dotenv version 0.21.0  
python requests version 2.28.1  
jsonschema version 4.16.0  
scikit-learn version 1.1.3  
matplotpib version 3.5.3  
hvplot version 0.8.2  

Note: you will need access to Blockspan's API in order to execute the API call. This platform can be found at https://blockspan.com/

---

## Installation Guide

To check your current Python version, run the following code in your terminal:  
python --version   
  
To check if the aforementioned packages are installed on your local machine, use the following code:  
conda list python-dotenv  
conda list requests  
conda list jsonschema  
conda list scikit-learn  
conda list matplotlib  
conda list hvplot  

If installation of these packages is required, run pip install or conda install on your local machine. 

---

## Usage

Important: This program, the code, and the files housed in this repository are intended purely for academic purposes. They are solely an example of what is possible and are not intended to provide actual investment advice. 

The "Supervised_Learning_Classification_Model.ipynb" is the file used to call the API data from Blockspan.com. The goal of this program is to advise the Happy Monkey user of top moving collections in the presentand near future. The file will pull the data into a Pandas DataFrame and identify the top moving collections. Train and test variables are created from the data to be fed into a Supervised Learning model (specifically, Logistical Regression). Training and testing reports are given. The long-term goal of this part of the program is to predict top moving collections in the near future. Further tuning of the algorithm, using the API call, will allow the real-time data to aid in these efforts. 

The "Top_5_Collections_Analysis.ipynb" file contains the code for the trading algorithm. The goal of this algorithm is to advise the Happy Monkey user whether or not to buy/sell one of the top moving collections. In this program, historical data is pulled into DataFrames. The data is then prepped for analysis, split into training and testing variables, and applied to an SVM regression model. Classification reports are given and visuals are provided to assess the algorithm's performance. Although further fine-tuning is required, the overall algorithm (applied consistently to all 5 collections) yielded positive ETH returns! 

As an interface for the Happy Monkey user, a chatbot has been created using AWS's AmazonLex. The "lambda_for_NFT.txt" file is an exemplification of the bot's communication logic. The "price5nft.txt" file houses the data for the Top 5 Collections (identified on Dec. 15th, 2022) for use in the chatbot. Here is an example fo the chatbot aiding a user in selecting one of the five NFT collections:   

Investor: I want to invest  
Bot: Are you interested in an NFT (Non-Fungible Token)?  
Investor: yes,  
Bot: The top five are: Cryptopunks, Azuki, BoredApeYachtClub,
         CloneX,and PudgyPenguins:want to continue?  
Investor: yes  
Bot: Which one do you prefer: n1) Cryptopunks, n2) Azuki, n3) Bored Ape Yacht  
     Club, n4) CloneX, or n5) PudgyPenguins?  
Investor: n2  
Bot: How much do you want to buy (in USD)?  
Investor: 5k  
Bot: This is to confirm that you will invest $5000 to buy "Azuki" NFT. Is this correct?  
Investor: yes  
Bot:  Name        floorPriceETH price_USD   MktCap_USD Volume_USD  
    Rank 2 Azuki 0.000005       $0.00591687 $150,685    $1,595  
    
---

## Contributors

Shahrukh Alam  
Alexandra Paiz  
Yan Huang  
Paul Yan  
Brock Denton  

---

## License

Columbia Engineering: FinTech Bootcamp, Aug. 2022 - Feb. 2023