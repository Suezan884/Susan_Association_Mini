# Susan_Association_Mini
# Data simulation
Created 10 fake transactions using a random combination of the following items:
Bread, Milk, Eggs, Banana, Chicken, Juice, Peanut, Cooking Oil


# Analysis
Used one-hot encoding with pandas, then applied the Apriori algorithm via mlxtend to detect frequent itemsets with a minimum support of 30%.

Generated association rules using:

Metric: confidence

Minimum threshold: 0.7

#  Chosen rule
Antecedents: (milk, banana) Consequents: (Bread) Support: 0.3 → The rule applies to 30% of all transactions Confidence: 1.00 → 100% of the time, when someone buys milk and banana, they also buy bread Lift: 2.0 → This purchase combo happens twice as often as it would randomly

# What it means in real life
In everyday shopping terms:
Every customer who buys milk and bananas also buys bread.

This tells us there's a strong relationship between these three items. A retailer could use this insight to:
Place bread close to milk and bananas to make it more accessible
Bundle them into a combo deal or promotion
Forecast stock based on increased demand when milk and bananas sell

In short, if a shopper grabs milk and bananas, the store can reliably expect them to also pick up bread. So it's a great chance to design smarter layouts or marketing strategies.

