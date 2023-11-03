# Market-Basket-Analysis

Market Basket Analysis is one of the key techniques used by large retailers to uncover associations between items. It works by looking for combinations of items that occur together frequently in transactions. To put it another way, it allows retailers to identify relationships between the items that people buy.

![image](https://github.com/basel-ay/Market-Basket-Analysis/assets/64821137/94b2b662-9c9f-44cd-bc66-c13fa5042bce)

Association Rules are widely used to analyze retail basket or transaction data and are intended to identify strong rules discovered in transaction data using measures of interestingness, based on the concept of strong rules.

<p align="center">
  <img src="https://github.com/basel-ay/Market-Basket-Analysis/assets/64821137/52e8e93a-6ac5-4c26-9504-825286b1b5c6"/>
</p>

An example of Association Rules, assume there are 100 customers

* 10 of them bought milk, 8 bought butter and 6 bought both of them.
* bought milk => bought butter
* support = P(Milk & Butter) = 6/100 = 0.06
* confidence = support/P(Butter) = 0.06/0.08 = 0.75
* lift = confidence/P(Milk) = 0.75/0.10 = 7.5

Association rules are normally written like this: {Diapers} -> {Beer} which means that there is a strong relationship between customers that purchased diapers and also purchased beer in the same transaction.

In the above example, the {Diaper} is the antecedent and the {Beer} is the consequent. Both antecedents and consequents can have multiple items. In other words, {Diaper, Gum} -> {Beer, Chips} is a valid rule.

**Support** is a measure that indicates how frequently an itemset (or combination of items) appears in the dataset. It is calculated as the number of transactions containing the itemset divided by the total number of transactions. High support values indicate that the itemset is commonly purchased or occurs together.

**Confidence**  is a measure of the likelihood that if a customer purchases one item from an itemset, they will also purchase another item from the same itemset. It is calculated as the support of the combination of items divided by the support of the antecedent item. High confidence values suggest a strong association between items.

**Lift** is a measure that helps determine whether an association between items is stronger than what would be expected by chance. It is calculated as the confidence of the itemset divided by the support of the consequent item. A lift value greater than 1 suggests a positive association, while a lift value less than 1 implies a negative association.

This analysis requires that all the data for a transaction be included in 1 row and the items should be 1-hot encoded,

![image](https://github.com/basel-ay/Market-Basket-Analysis/assets/64821137/45027e2d-2790-44b8-91e2-7cd15116af3f)

The specific data for this article comes from the UCI Machine Learning Repository and represents transactional data from a UK retailer from 2010-2011. This mostly represents sales to wholesalers so it is slightly different from consumer purchase patterns but is still a useful case study.
