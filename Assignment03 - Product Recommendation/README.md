# Product Recomment
## Dataset
A survey asking whether or not the user (students from the class) has ever purchased/used an item. We received 29 responses, and each respondent rated each item from 26 items as Yes or No.

### Notebook :[Product Recommendation](https://github.com/panita10/BADS7105-CRM-Analytics/blob/main/Assignment03%20-%20Product%20Recommendation/Product_Recommendation.ipynb)
### Colab :[Product Recommendation](https://colab.research.google.com/drive/1AZ3lNBjEtpYCSto9UxHRRqbq9r8AUmtA)

## Top Least common items
To see how common (ever purchased by users) each item is

![image](https://user-images.githubusercontent.com/92771399/147726824-abece44f-edb1-40fa-886d-f65c02dcc042.png)

## Association Rules
the visualization of 1-itemset association rules (filtered by Support > 0.4 and Lift > 1) Nodes represent items and directed edges represent rules (antecedents ➞ consequents). Edge labels annotates Lift values. Note that for 1-to-1-itemset, both directions of rules (A➞B, B➞A) have the same lift values.

![image](https://user-images.githubusercontent.com/92771399/147726869-82a0e96f-652c-4ec1-af14-72b949fd818d.png)

## Collaborative Filtering - Item Similarity
By using users' ratings for each item as its feature vector, calculates cosine similarity values for each pair of items. We could recommend items based on item similarity. Filtering the similarity using 0.65 threshold, and visualize them in graph. A node represents an item. Edge thickness and color represent cosine similarity between 2 items.
![image](https://user-images.githubusercontent.com/92771399/147726908-c2e504ac-5ded-4035-a12b-81d5c3f1e51a.png)
![image](https://user-images.githubusercontent.com/92771399/147726919-3055160e-3667-48df-a778-557079fabe2d.png)
