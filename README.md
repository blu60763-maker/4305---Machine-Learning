The goal of this project is to build a fair-value rental pricing framework using the Apartment
for Rent Classified dataset. The project first standardizes listing prices to a monthly basis,
then uses cleaned and transformed listing information to estimate the expected monthly rent
of each unit. Based on the difference between the actual listed price and model-predicted
price, the system further classifies listings into practical pricing bands such as Deal, Fair, and
Premium. This allows the output to be interpreted not only as a prediction task, but also as a
decision-support tool.

To make the analysis more useful, this project pays particular attention to two important
aspects of rental pricing: geographic location and amenities. Location may influence rental
value through local market conditions that are not fully captured by simple city or state
labels, while amenities may reflect differences in housing quality and tenant appeal. By
examining these factors alongside core structural features, the project aims to produce a more
informative and practically useful pricing benchmark.

Overall, this project is designed as an end-to-end data science pipeline that connects data
understanding, preprocessing, exploratory analysis, modeling, and interpretation. Rather than
focusing only on model accuracy, the project emphasizes decision value: whether the
resulting system can provide stakeholders with a more consistent and evidence-based way to
evaluate rental prices.
