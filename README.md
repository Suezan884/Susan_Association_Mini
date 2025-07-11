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

# Output
[['banana', 'eggs', 'peanut'], ['banana', 'peanut', 'chicken', 'Bread'], ['milk', 'cooking oil', 'juice', 'Bread', 'banana'], ['chicken', 'banana'], ['eggs', 'banana', 'cooking oil'], ['milk', 'cooking oil', 'eggs'], ['milk', 'cooking oil', 'banana', 'Bread', 'chicken'], ['eggs', 'Bread'], ['banana', 'Bread', 'milk'], ['milk', 'eggs', 'cooking oil']]
    support               itemsets
0       0.5                (Bread)
1       0.7               (banana)
2       0.3              (chicken)
3       0.5          (cooking oil)
4       0.5                 (eggs)
5       0.5                 (milk)
6       0.4        (Bread, banana)
7       0.3          (milk, Bread)
8       0.3      (chicken, banana)
9       0.3  (cooking oil, banana)
10      0.3         (milk, banana)
11      0.3    (eggs, cooking oil)
12      0.4    (milk, cooking oil)
13      0.3  (milk, Bread, banana)
       antecedents    consequents  support  confidence      lift
0          (Bread)       (banana)      0.4        0.80  1.142857
1        (chicken)       (banana)      0.3        1.00  1.428571
2           (milk)  (cooking oil)      0.4        0.80  1.600000
3    (cooking oil)         (milk)      0.4        0.80  1.600000
4    (milk, Bread)       (banana)      0.3        1.00  1.428571
5   (milk, banana)        (Bread)      0.3        1.00  2.000000
6  (Bread, banana)         (milk)      0.3        0.75  1.500000